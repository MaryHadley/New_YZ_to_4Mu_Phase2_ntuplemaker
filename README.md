#To get the code   
mkdir < workArea  >  
cd < workArea >   
cmsrel CMSSW_10_6_27   
cd CMSSW_10_6_27/src  
git clone git@github.com:MaryHadley/New_YZ_to_4Mu_Phase2_ntuplemaker.git  
cd New_YZ_to_4Mu_Phase2_ntuplemaker  
mv * ..  
cd ..  
rm -rf New_YZ_to_4Mu_Phase2_ntuplemaker   
cmsenv

#To run Z + Y --> 4 mu looper:   
root -l -b  
.L new_workInProgress_clean_flexible_loop_ZplusY.C++  
run("< nameOfFil e>.root")   

#To run Z->4 mu looper  
root -l -b  
.L clean_flexible_loop_Zto4Mu_JanCutsRemoved.C++  
run("< nameOfFile >.root")   
