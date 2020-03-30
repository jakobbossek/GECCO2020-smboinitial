Explanation of datasets results_{xy,y}.csv
===

x-values are d-dimensional numeric vectors and y-values are the corresponding images
in objective space, i.e, y.something = f(x.something) where f is the BBOB(fid, iid, dimension)
function.

Notes
===

results_xy.csv contains all the following columns while results_y.csv contains
all columns expect for the x.* columns.

Description of columns
===

"y.best.initial.design": best y-value in initial design
"x.best.initial.design": best x-value in initial design
"y.best": overall best y-value after SMBO finished
"x.best": overall best x-value after SMBO finished
"y.best.onestep": best y-value after single SMBO step (one-shot with one additional evaluation)
"x.best.onestep": best x-value after single SMBO step
"x.dist": Distance (L2-norm) from x.best to x.opt
"y.dist": Distance from y.best to y.opt, i.e., y.best - y.opt >= 0
"x.opt": optimal x-value, i.e., global optimum
"y.opt": optimal y-value
"method": Initial design method form {Halton, LHS, Sobol, Uniform}
"dimension": BBOB problem dimension, i.e., dimension of decision space
"size": Size of initial design (equals budget initial)
"id": filename of design (this can be used to map discrepancy values later on in a join operation)
"path.to.design": relative path to design in repository from the experiments/ folder
"fid": BBOB function ID
"iid": BBOB instance ID
"budget.total": overall budget
"budget.initial.ratio": fraction of budget.total used for initial design
"budget.initial": budget used for initial design
"repl": Independent replication of SMBO given all other parameters are fixed
"discrepancy": (approximated) star discrepancy value for the used design
