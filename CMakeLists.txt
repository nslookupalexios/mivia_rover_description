cmake_minimum_required(VERSION 3.5)
project(mivia_rover_description)

# ====================================================================
# Dependencies
# ====================================================================

find_package(ament_cmake REQUIRED)

# ====================================================================
# Install
# ====================================================================

# Install URDF/Xacro files
install(
  DIRECTORY urdf
  DESTINATION share/${PROJECT_NAME}
)

# Install meshes (visual + collision)
install(
  DIRECTORY meshes
  DESTINATION share/${PROJECT_NAME}
)

# Install RViz configurations
install(
  DIRECTORY rviz
  DESTINATION share/${PROJECT_NAME}
)

# ====================================================================
# Package
# ====================================================================

ament_package()