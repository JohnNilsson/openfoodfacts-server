This file describes the fields from the CSV export of the products in the Open Food Facts database.

See https://world.openfoodfacts.org/data for more information.

The file encoding is Unicode UTF-8. The character that separates fields is <tab> (tabulation).

# Generalities

- fields that end with `_t` are dates in the UNIX timestamp format (number of seconds since Jan 1st 1970)
- fields that end with `_datetime` are dates in the iso8601 format: `yyyy-mm-ddThh:mn:ssZ`
- fields that end with `_tags` are comma separated list of tags (e.g. `categories_tags` is the set of normalized tags computed from the `categories` field)
- fields that end with a language 2 letter code (e.g. `fr` for French) is the set of tags in that language
- fields that end with `_100g` correspond to the amount of a nutriment (in g, or kJ for energy) for 100 g or 100 ml of product
- fields that end with `_serving` correspond to the amount of a nutriment (in g, or kJ for energy) for 1 serving of the product

# List of fields

## general information

- `code`
  - barcode of the product (can be EAN-13 or internal codes for some food stores); for products without a barcode, Open Food Facts assigns a number starting with the 200 reserved prefix
  - example: `3560070349746`
- `url`
  - url of the product page on Open Food Facts
  - example: `https://world-en.openfoodfacts.org/product/3560070349746/camembert-21-mg-simpl`
- `creator`
  - contributor who first added the product. `openfoodfacts-contributors` means an anonymous contributor.
  - example: `stephane`
- `created_t`
  - date that the product was added (UNIX timestamp format)
  - example: `1587670000`
- `created_datetime`
  - date that the product was added (iso8601 format: yyyy-mm-ddThh:mn:ssZ). It is generated from `created_t`
  - example: `2020-04-23T19:26:40Z`
- `last_modified_t`
  - date that the product page was last modified (UNIX timestamp format)
  - example: `1587670000`
- `last_modified_datetime`
  - date that the product was last modified (iso8601 format: yyyy-mm-ddThh:mn:ssZ). It is generated from `last_modified_t`
  - example: `2020-04-23T19:26:40Z`
- `product_name`
  - name of the product as printed on the packaging
  - example: `Super bar plus-plus`
- `abbreviated_product_name`
- `generic_name`
  - generic name of the product
  - example: `Cereal bars`
- `quantity`
  - quantity and unit
  - example: `1 BAR (62 g)`

## tags

- `packaging` : shape, material
- `packaging_tags`
- `packaging_en`
- `packaging_text`
- `brands`
- `brands_tags`
- `categories`
- `categories_tags`
- `categories_en`
- `origins` : origins of ingredients
- `origins_tags`
- `origins_en`
- `manufacturing_places` : places where manufactured or transformed
- `manufacturing_places_tags`
- `labels`
- `labels_tags`
- `labels_en`
- `emb_codes`
- `emb_codes_tags`
- `first_packaging_code_geo` : coordinates corresponding to the first packaging code indicated
- `cities`
- `cities_tags`
- `purchase_places`
- `stores`
- `countries` : list of countries where the product is sold
- `countries_tags`
- `countries_en`

## ingredients

- `ingredients_text`
- `ingredients_tags`
- `ingredients_analysis_tags`
- `allergens`
- `allergens_en`
- `traces`
- `traces_tags`
- `traces_en`

## misc. data

- `serving_size` : text describing the serving size
- `serving_quantity` : normalized serving size in grams or ml
- `no_nutriments` : indicates if the nutrition facts are indicated on the food label
- `additives_n` : number of food additives
- `additives`
- `additives_tags`:
  - normalized list of the additives contained in the product. It is automatically generated from `ingredients_text`.
  - example: `en:e296,en:e330,en:e552,en:e950,en:e955`
- `additives_en`
- `nutriscore_score`
  - nutrition grade ('a' to 'e'). see https://fr.openfoodfacts.org/nutriscore
- `nutriscore_grade`
- `nova_group`
- `pnns_groups_1`
- `pnns_groups_2`
- `food_groups`
- `food_groups_tags`
- `food_groups_en`
- `states`
- `states_tags`
- `states_en`
- `brand_owner`
- `ecoscore_score`
- `ecoscore_grade`
- `nutrient_levels_tags`
- `product_quantity`   
- `owner`
- `data_quality_errors_tags`
- `unique_scans_n`
- `popularity_tags`
- `completeness`
- `last_image_t`
- `last_image_datetime`
- `main_category`
- `main_category_en`
- `image_url`
- `image_small_url`
- `image_ingredients_url`
- `image_ingredients_small_url`
- `image_nutrition_url`
- `image_nutrition_small_url`

## nutrition facts

Please see https://wiki.openfoodfacts.org/Nutrients_handling_in_Open_Food_Facts for more information on nutrients.

- `energy-kj_100g`
- `energy-kcal_100g`
- `energy_100g`
- `energy-from-fat_100g`
- `fat_100g`
- `saturated-fat_100g`
- `-butyric-acid_100g`
- `-caproic-acid_100g`
- `-caprylic-acid_100g`
- `-capric-acid_100g`
- `-lauric-acid_100g`
- `-myristic-acid_100g`
- `-palmitic-acid_100g`
- `-stearic-acid_100g`
- `-arachidic-acid_100g`
- `-behenic-acid_100g`
- `-lignoceric-acid_100g`
- `-cerotic-acid_100g`
- `-montanic-acid_100g`
- `-melissic-acid_100g`
- `monounsaturated-fat_100g`
- `polyunsaturated-fat_100g`
- `omega-3-fat_100g`
- `-alpha-linolenic-acid_100g`
- `-eicosapentaenoic-acid_100g`
- `-docosahexaenoic-acid_100g`
- `omega-6-fat_100g`
- `-linoleic-acid_100g`
- `-arachidonic-acid_100g`
- `-gamma-linolenic-acid_100g`
- `-dihomo-gamma-linolenic-acid_100g`
- `omega-9-fat_100g`
- `-oleic-acid_100g`
- `-elaidic-acid_100g`
- `-gondoic-acid_100g`
- `-mead-acid_100g`
- `-erucic-acid_100g`
- `-nervonic-acid_100g`
- `trans-fat_100g`
- `cholesterol_100g`
- `carbohydrates_100g`
- `sugars_100g`
- `-sucrose_100g`
- `-glucose_100g`
- `-fructose_100g`
- `-lactose_100g`
- `-maltose_100g`
- `-maltodextrins_100g`
- `starch_100g`
- `polyols_100g`
- `fiber_100g`
- `soluble-fiber_100g`
- `insoluble-fiber_100g`
- `proteins_100g`
- `casein_100g`
- `serum-proteins_100g`
- `nucleotides_100g`
- `salt_100g`
- `sodium_100g`
- `alcohol_100g`
- `vitamin-a_100g`
- `beta-carotene_100g`
- `vitamin-d_100g`
- `vitamin-e_100g`
- `vitamin-k_100g`
- `vitamin-c_100g`
- `vitamin-b1_100g`
- `vitamin-b2_100g`
- `vitamin-pp_100g`
- `vitamin-b6_100g`
- `vitamin-b9_100g`
- `folates_100g`
- `vitamin-b12_100g`
- `biotin_100g`
- `pantothenic-acid_100g`
- `silica_100g`
- `bicarbonate_100g`
- `potassium_100g`
- `chloride_100g`
- `calcium_100g`
- `phosphorus_100g`
- `iron_100g`
- `magnesium_100g`
- `zinc_100g`
- `copper_100g`
- `manganese_100g`
- `fluoride_100g`
- `selenium_100g`
- `chromium_100g`
- `molybdenum_100g`
- `iodine_100g`
- `caffeine_100g`
- `taurine_100g`
- `ph_100g`
- `fruits-vegetables-nuts_100g`
- `fruits-vegetables-nuts-dried_100g`
- `fruits-vegetables-nuts-estimate_100g`
- `fruits-vegetables-nuts-estimate-from-ingredients_100g`
- `collagen-meat-protein-ratio_100g`
- `cocoa_100g`
- `chlorophyl_100g`
- `carbon-footprint_100g`
- `carbon-footprint-from-meat-or-fish_100g`
- `nutrition-score-fr_100g`
- `nutrition-score-uk_100g`
- `glycemic-index_100g`
- `water-hardness_100g`
- `holine_100g`
- `phylloquinone_100g`
- `beta-glucan_100g`
- `inositol_100g`
- `carnitine_100g`
