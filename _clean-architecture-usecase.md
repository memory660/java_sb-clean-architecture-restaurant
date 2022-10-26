```
infrastructure                                  domain                                      domain                              infrastructure
api                                             usecase                                     repository                          repository
RestaurantController                            GetRestaurantsUseCase                       RestaurantRepository                RestaurantRepositoryImpl 
                                                                                                                                        implements RestaurantRepository
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------



@GetMapping(value = "/restaurants")
    getRestaurantsUseCase.execute(input) ---->  execute(GetRestaurantsInput input) {        interface RestaurantRepository {    findAll(...) {
        .map(RestaurantResponse::of)                return restaurantRepository     ----->     findAll(...);           -------->    ...
                                                        .findAll(input.toEntity());                                                 ...
                                                }


```

