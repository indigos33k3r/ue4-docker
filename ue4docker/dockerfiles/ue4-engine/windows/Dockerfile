# escape=`
ARG TAG
FROM adamrehn/ue4-source:${TAG}

# Build UBT and build the Engine
RUN GenerateProjectFiles.bat
RUN .\Engine\Build\BatchFiles\Build.bat UE4Editor Win64 Development -WaitMutex
RUN .\Engine\Build\BatchFiles\Build.bat ShaderCompileWorker Win64 Development -WaitMutex
RUN .\Engine\Build\BatchFiles\Build.bat UnrealPak Win64 Development -WaitMutex
