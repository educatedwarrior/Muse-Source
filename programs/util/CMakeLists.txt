add_executable( get_dev_key get_dev_key.cpp )

target_link_libraries( get_dev_key
                       PRIVATE muse_app muse_chain muse_egenesis_full graphene_utilities fc ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )

install( TARGETS
   get_dev_key

   RUNTIME DESTINATION bin
   LIBRARY DESTINATION lib
   ARCHIVE DESTINATION lib
)

add_executable( sign_digest sign_digest.cpp )

target_link_libraries( sign_digest
                       PRIVATE muse_app muse_chain muse_egenesis_full graphene_utilities fc ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )

install( TARGETS
   sign_digest

   RUNTIME DESTINATION bin
   LIBRARY DESTINATION lib
   ARCHIVE DESTINATION lib
)

add_executable( sign_transaction sign_transaction.cpp )

target_link_libraries( sign_transaction
                       PRIVATE muse_app muse_chain muse_egenesis_full graphene_utilities fc ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )

install( TARGETS
   sign_transaction

   RUNTIME DESTINATION bin
   LIBRARY DESTINATION lib
   ARCHIVE DESTINATION lib
)

add_executable( inflation_model inflation_model.cpp )
target_link_libraries( inflation_model
                       PRIVATE muse_chain muse_egenesis_full fc ${CMAKE_DL_LIBS} ${PLATFORM_SPECIFIC_LIBS} )

install( TARGETS
   inflation_model

   RUNTIME DESTINATION bin
   LIBRARY DESTINATION lib
   ARCHIVE DESTINATION lib
)
