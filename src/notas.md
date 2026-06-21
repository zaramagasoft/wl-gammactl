compilar
gcc main2.c wlr-gamma-control-unstable-v1-client-protocol.c -o motor_gamma -lwayland-client -lm

ejecutar terminal 1
./motor_gamma
Servicio Gamma iniciado. Escuchando en /tmp/gamma_pipe

otra shell
echo "b 1.3" > /tmp/gamma_pipe

1. Desde la Terminal (Para probar)
   Puedes enviar las letras b (brillo), c (contraste) o g (gamma) seguidas del valor que quieras:

Brillo (b): Controla la luminosidad general (0.0 a 1.0 es lo normal, más de 1.0 satura).

Bash
echo "b 0.8" > /tmp/gamma_pipe
Contraste (c): Controla la diferencia entre claros y oscuros (1.0 es normal, 1.5 es alto, 0.5 es lavado).

Bash
echo "c 1.2" > /tmp/gamma_pipe
Gamma (g): Controla la curva de tonos medios (1.0 es normal, 0.8 oscurece los grises, 1.2 los aclara).

Bash
echo "g 0.9" > /tmp/gamma_pipe