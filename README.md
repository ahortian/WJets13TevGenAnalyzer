-- Instructions

mkdir WJets13TeVGeN

cd WJets13TeVGeN

cmsrel CMSSW_7_6_4 

cd CMSSW_7_6_4/src

cmsenv 

voms-proxy-init -voms cms   // to acsess file in das

-- Clone /WJets13TevGenAnalyzer from the github

git clone https://github.com/ahortian/WJets13TevGenAnalyzer.git

-- Go to the directory 

cd WJets13TevGenAnalyzer

-- Run

scram b -j10

cmsRun wjets13tevanalyzer_cfg.py

-- for submitting crab jobs 

source /cvmfs/cms.cern.ch/crab3/crab.sh

crab submit --config=crabConfig_WJetsAMCNLO.py

