# Proof for orthogonal_matrices_is_group_TCC2
An error occurred while trying to save your proof in PVS.
If the problem persists, please report an issue on [github](https://github.com/nasa/vscode-pvs/issues) or on the [PVS group](https://groups.google.com/g/pvs-group), we will look into it.

## Your proof attempt
Don't panic, your proof attempt for orthogonal_matrices_is_group_TCC2 is not lost.<br>
VSCode-PVS saved your proof attempt, and you can restore it from the Proof Explorer menu **...** -> **Restore Proof**<br>

If everything else fails, below you can find the complete proof script, which you can paste in the prover terminal to repeat the proof:
```lisp
(skeep)(lemma "square_mult")(inst -1 "n" "x1`1" "x1`2")(flatten)(assert)(expand "*" -)(assert)(flatten)(skeep)(assert)(prop)(typepred "x1`2")
```