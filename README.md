# IC-Compiler-2

 IC Compiler Commands
#start GUI
icc_shell>start_gui
#report max transition constraints
icc_shell> report_constraint -max_transition -verbose
#report timing with transition with pins (through that pin)
icc_shell> report_timing -thr <instance_name>/<pin_name>
#report timing from register clk to d of next flipflop
icc_shell> report_timing -to <instance1_name>/<pin_name> -from <instance2_name>/clk
#see complete clock path
icc_shell>report_timing -to <pin_name> -path_type full_clock_expanded -delay max
#high light path in GUI
icc_shell>change_selection [get_timing_paths -to <instace_name>/<pin>]
#see clock tree information
icc_shell>report_clock_tree
#shows the worst path timing with the given clock
icc_shell>report_timing -group <group_name>
#prints only end points
icc_shell>report_timing -to readary -path_type short -max_paths 5
#summary of all
icc_shell>report_qor
#insert buffer
icc_shell>insert_buffer <instance_name>/d -lib_cell <lib_name>
#insert clock inverters
icc_shell>insert_buffer <instance_name>/<clk pin> -lib_cell <lib inverter>
-inverter_pair
#legalize placement incrementally
icc_shell>legalize_placement -incremental
#list the lib cells
icc_shell>get_lib_cell
#set false path
icc_shell>set_false_path -from <instance1_name>/<pin_name> -to
<instance2_name>/<pin_name>
#list of all cells matching with instance name and also sequencial elements
>get_cells *<name>* -filter "is_sequential==true"
#finding sizeof of collection
>sizeof_collections [get_cells *<name>* -filter "is_sequential==true"]
#show the terminal names
>get_terminals *<name>*
#check the direction of port

