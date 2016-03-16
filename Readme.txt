Rijndael’s Key Schedule
———————————————————————

This program demonstrates Rijndael’s key scheduling to expand a short key into a number of separate round keys. In this demo, we use the 128-bit key invariant.

Rcon
————

Rcon is what the Rijndael documentation calls the exponentiation of 2 to a user-specified value. Note that this operation is not performed with regular integers, but in Rijndael's finite field. In polynomial form, 2 is 2 = 00000010 = 0 * x^7 + 0 * x^6 + 0 * x^5 + 0 * x^4 + 0 * x^3 + 0 * x^2 + 1 * x + 0 = x and we compute rcon(i) = x^(i-1).

Equivalently, rcon(i) = x^(i-1) mod x^8 + x^4 + x^3 + x + 1 where i is taken as round number