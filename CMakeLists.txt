cmake_minimum_required(VERSION 3.12)
project(Tree)


set(CMAKE_CONFIGURATION_TYPES "Debug;Release" CACHE STRING "Configs" FORCE) #Создается переменная CMAKE_CONFIGURATION_TYPES со значением "Debug;Release" и меткой/разделом Configs, переменная сохраниется в специальном файле доступном из всех файлов,
if(NOT CMAKE_BUILD_TYPE) # проверка имеющихся у компилятора вариантов сборки
  set(CMAKE_BUILD_TYPE Release) #Если нет то устанавливаем Release
endif()

add_subdirectory(gtest)
add_subdirectory(Node)
add_subdirectory(TreeNode)
add_subdirectory(Tree)
add_subdirectory(LabTest)

