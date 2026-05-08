# Proof for ortho_is_linear_isometry
An error occurred while trying to save your proof in PVS.
If the problem persists, please report an issue on [github](https://github.com/nasa/vscode-pvs/issues) or on the [PVS group](https://groups.google.com/g/pvs-group), we will look into it.

## Your proof attempt
Don't panic, your proof attempt for ortho_is_linear_isometry is not lost.<br>
VSCode-PVS saved your proof attempt, and you can restore it from the Proof Explorer menu **...** -> **Restore Proof**<br>

If everything else fails, below you can find the complete proof script, which you can paste in the prover terminal to repeat the proof:
```lisp
(skeep)(expand "linear_isometry?")(split)(expand "isometry?")(skosimp)(lemma "matv_dist_sub")(inst - "A" "x!1" "y!1")(case "mult(A, x!1 - y!1) = mult(A, x!1) - mult(A, y!1)")(hide -2)(expand "norm_2" 1)(expand "norm_2sq" 1)(lemma "ortho_preserves_dot")(inst - "A" "x!1 - y!1" "x!1 - y!1")(expand "*" 1)(replace -2 :dir RL)(expand "*" -1)(replace -1 1)(propax)(hide -1 2)(typepred "x!1")(typepred "y!1")(lemma "length_add_vect_same")(expand "-" 1)(expand "sub" 1)(inst -1 "x!1" "scal(-1, y!1)")(expand "+" -1)(hide -2 -5)(lemma "length_scal_vect")(inst -1 "-1" "y!1")(expand "*" -1)(assert)(lemma "mmult_sub_dist" ("m" "n" "n" "n" "A" "A" "v1" "x!1" "v2" "y!1"))(expand "mult" -1)(propax)(typepred "A")(assert)(expand "rows" -6)(assert)(skolem!)(lemma "matrices.length_row")(inst? -1)(inst -1 "i!1")(expand "row" -1)(assert)(expand "fixes_origin?")(lemma "matv_zerovec")(inst -1 "A")(typepred "A")(replace -6 -5)(replace -6 -8)(replace -5 -8 :dir RL)(hide-all-but (-8 1))(expand "*")(hide-all-but (-1 -2 -3 -4 -5 -6 -7))(expand "*")(assert)(replace -6 -5)(replace -5 -8 :dir RL)(hide -1 -2 -3 -4 -5 -6 -7)(case "zero(n) = zero_vec(n)")(replace -1 -2 :dir RL)(postpone)(postpone)
```