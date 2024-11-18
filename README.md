[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/9gm_-fkT)

[Contracting Goals](https://www.sba.gov/partners/contracting-officials/small-business-procurement)
The combined goals for the federal government are:

- 23% of prime contracts for small businesses
- 5% of prime and subcontracts for women-owned small businesses
- 5% of prime contracts and subcontracts for small disadvantaged businesses
- 3% of prime contracts and subcontracts for HUBZone small businesses
- 3% of prime and subcontracts for service-disabled veteran-owned small businesses

[Contracting Goals by government agency](https://www.sba.gov/document/support-agency-contracting-goals)

FY23: 6,677,459 rows

- Time frame
    action_date
    action_date_fiscal_year
- Agency
    awarding_agency_code
    awarding_agency_name
- Award type
    award_type
    award_type_code
- Recipient
    recipient_uei
    recipient_name
    cage_code
    recipient_address_line_1
    recipient_address_line_2
    recipient_city_name
    recipient_state_code
    recipient_zip_4_code
    
- Recipient-Type
- Award Amount: federal_action_obligation
- NAICS
    naics_code
    naics_description
- PSC
    product_or_service_code
    product_or_service_code_description
- Type of Set-Aside
    type_of_set_aside_code
    type_of_set_aside
    service_disabled_veteran_owned_business
    women_owned_small_business
    historically_underutilized_business_zone_hubzone_firm
- Place of performance
    primary_place_of_performance_country_code
    primary_place_of_performance_city_name
    primary_place_of_performance_county_name
    primary_place_of_performance_state_code
    primary_place_of_performance_zip_4

1. Does the Federal Government meet its contracting goals?
2. Do each of the federal agencies meet their contracting goal?
3. Which NAICS receives the most small business $?
4. Which PSC receives the most small business $?
5. $ evenly distributed by NAICS? (total receipeints vs AvG contracts per recpient)
6. $ evenly distributed by PSC? (total receipeints vs AvG contracts per recpient)
7. $ performed in the Houson area(by local zip codes)
8. Houston Place of performance vs Recipient Location
9. $ evenly distributed in the Houston area

ANC: Alaska Native Corporation
CDC: Community Development Corporations
NHO: Native Hawaiian Organizations
contracting_officers_determination_of_business_size
contracting_officers_determination_of_business_size_code
alaskan_native_corporation_owned_firm
american_indian_owned_business
native_hawaiian_organization_owned_firm
minority_owned_business
subcontinent_asian_asian_indian_american_owned_business
asian_pacific_american_owned_business
black_american_owned_business
hispanic_american_owned_business
native_american_owned_business
other_minority_owned_business

```SQL
CREATE TABLE FY2023_All_Contracts_Full_20241107(
	contract_transaction_unique_key TEXT,
	federal_action_obligation REAL,
	action_date TEXT,
	action_date_fiscal_year INTEGER,
	awarding_agency_code INTEGER,
	awarding_agency_name TEXT,
	recipient_uei TEXT,
	recipient_name TEXT,
	cage_code TEXT,
	recipient_country_code TEXT,
	recipient_country_name TEXT,
	recipient_address_line_1 TEXT,
	recipient_address_line_2 TEXT,
	recipient_city_name TEXT,
	recipient_county_name TEXT,
	recipient_state_code TEXT,
	recipient_state_name TEXT,
	recipient_zip_4_code INTEGER,
	primary_place_of_performance_country_code TEXT,
	primary_place_of_performance_country_name TEXT,
	primary_place_of_performance_city_name TEXT,
	primary_place_of_performance_county_name TEXT,
	primary_place_of_performance_state_code TEXT,
	primary_place_of_performance_state_name TEXT,
	primary_place_of_performance_zip_4 TEXT,
	award_or_idv_flag TEXT,
	award_type_code TEXT,
	award_type TEXT,
	idv_type_code TEXT,
	idv_type TEXT,
	product_or_service_code TEXT,
	product_or_service_code_description TEXT,
	naics_code INTEGER,
	naics_description TEXT,
	place_of_manufacture_code TEXT,
	place_of_manufacture TEXT,
	type_of_set_aside_code TEXT,
	type_of_set_aside TEXT,
	fed_biz_opps_code TEXT,
	fed_biz_opps TEXT,
	alaskan_native_corporation_owned_firm TEXT,
	american_indian_owned_business TEXT,
	native_hawaiian_organization_owned_firm TEXT,
	service_disabled_veteran_owned_business TEXT,
	women_owned_small_business TEXT,
	economically_disadvantaged_women_owned_small_business TEXT,
	minority_owned_business TEXT,
	subcontinent_asian_asian_indian_american_owned_business TEXT,
	asian_pacific_american_owned_business TEXT,
	black_american_owned_business TEXT,
	hispanic_american_owned_business TEXT,
	native_american_owned_business TEXT,
	other_minority_owned_business TEXT,
	contracting_officers_determination_of_business_size TEXT,
	contracting_officers_determination_of_business_size_code TEXT,
	community_developed_corporation_owned_firm TEXT,
	dot_certified_disadvantage TEXT,
	self_certified_small_disadvantaged_business TEXT,
	small_disadvantaged_business TEXT,
	historically_underutilized_business_zone_hubzone_firm TEXT
);
```

```SQL
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT () FROM FY2023_All_Contracts_Full_20241107_2;
DROP TABLE FY2023_All_Contracts_Full_20241107_2;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT * FROM FY2023_All_Contracts_Full_20241107_3;
DROP TABLE FY2023_All_Contracts_Full_20241107_3;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT * FROM FY2023_All_Contracts_Full_20241107_4;
DROP TABLE FY2023_All_Contracts_Full_20241107_4;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT * FROM FY2023_All_Contracts_Full_20241107_5;
DROP TABLE FY2023_All_Contracts_Full_20241107_5;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT * FROM FY2023_All_Contracts_Full_20241107_6;
DROP TABLE FY2023_All_Contracts_Full_20241107_6;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT * FROM FY2023_All_Contracts_Full_20241107_7;
DROP TABLE FY2023_All_Contracts_Full_20241107_7;
```

```SQL
CREATE TABLE FY2023_All_Contracts_Full_20241107(
	contract_transaction_unique_key TEXT,
	federal_action_obligation TEXT,
	action_date TEXT,
	action_date_fiscal_year TEXT,
	awarding_agency_code TEXT,
	awarding_agency_name TEXT,
	recipient_uei TEXT,
	recipient_name TEXT,
	cage_code TEXT,
	recipient_country_code TEXT,
	recipient_country_name TEXT,
	recipient_address_line_1 TEXT,
	recipient_address_line_2 TEXT,
	recipient_city_name TEXT,
	recipient_county_name TEXT,
	recipient_state_code TEXT,
	recipient_state_name TEXT,
	recipient_zip_4_code TEXT,
	primary_place_of_performance_country_code TEXT,
	primary_place_of_performance_country_name TEXT,
	primary_place_of_performance_city_name TEXT,
	primary_place_of_performance_county_name TEXT,
	primary_place_of_performance_state_code TEXT,
	primary_place_of_performance_state_name TEXT,
	primary_place_of_performance_zip_4 TEXT,
	award_or_idv_flag TEXT,
	award_type_code TEXT,
	award_type TEXT,
	idv_type_code TEXT,
	idv_type TEXT,
	product_or_service_code TEXT,
	product_or_service_code_description TEXT,
	naics_code TEXT,
	naics_description TEXT,
	place_of_manufacture_code TEXT,
	place_of_manufacture TEXT,
	type_of_set_aside_code TEXT,
	type_of_set_aside TEXT,
	fed_biz_opps_code TEXT,
	fed_biz_opps TEXT,
	alaskan_native_corporation_owned_firm TEXT,
	american_indian_owned_business TEXT,
	native_hawaiian_organization_owned_firm TEXT,
	service_disabled_veteran_owned_business TEXT,
	women_owned_small_business TEXT,
	economically_disadvantaged_women_owned_small_business TEXT,
	minority_owned_business TEXT,
	subcontinent_asian_asian_indian_american_owned_business TEXT,
	asian_pacific_american_owned_business TEXT,
	black_american_owned_business TEXT,
	hispanic_american_owned_business TEXT,
	native_american_owned_business TEXT,
	other_minority_owned_business TEXT,
	contracting_officers_determination_of_business_size TEXT,
	contracting_officers_determination_of_business_size_code TEXT,
	community_developed_corporation_owned_firm TEXT,
	dot_certified_disadvantage TEXT,
	self_certified_small_disadvantaged_business TEXT,
	small_disadvantaged_business TEXT,
	historically_underutilized_business_zone_hubzone_firm TEXT
);
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_1;
DROP TABLE FY2023_All_Contracts_Full_20241107_1;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_2;
DROP TABLE FY2023_All_Contracts_Full_20241107_2;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_3;
DROP TABLE FY2023_All_Contracts_Full_20241107_3;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_4;
DROP TABLE FY2023_All_Contracts_Full_20241107_4;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_5;
DROP TABLE FY2023_All_Contracts_Full_20241107_5;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_6;
DROP TABLE FY2023_All_Contracts_Full_20241107_6;
INSERT INTO FY2023_All_Contracts_Full_20241107 SELECT 
  contract_transaction_unique_key,
  federal_action_obligation,
  action_date,
  action_date_fiscal_year,
  awarding_agency_code,
  awarding_agency_name,
  recipient_uei,
  recipient_name,
  cage_code,
  recipient_country_code,
  recipient_country_name,
  recipient_address_line_1,
  recipient_address_line_2,
  recipient_city_name,
  recipient_county_name,
  recipient_state_code,
  recipient_state_name,
  recipient_zip_4_code,
  primary_place_of_performance_country_code,
  primary_place_of_performance_country_name,
  primary_place_of_performance_city_name,
  primary_place_of_performance_county_name,
  primary_place_of_performance_state_code,
  primary_place_of_performance_state_name,
  primary_place_of_performance_zip_4,
  award_or_idv_flag,
  award_type_code,
  award_type,
  idv_type_code,
  idv_type,
  product_or_service_code,
  product_or_service_code_description,
  naics_code,
  naics_description,
  place_of_manufacture_code,
  place_of_manufacture,
  type_of_set_aside_code,
  type_of_set_aside,
  fed_biz_opps_code,
  fed_biz_opps,
  alaskan_native_corporation_owned_firm,
  american_indian_owned_business,
  native_hawaiian_organization_owned_firm,
  service_disabled_veteran_owned_business,
  women_owned_small_business,
  economically_disadvantaged_women_owned_small_business,
  minority_owned_business,
  subcontinent_asian_asian_indian_american_owned_business,
  asian_pacific_american_owned_business,
  black_american_owned_business,
  hispanic_american_owned_business,
  native_american_owned_business,
  other_minority_owned_business,
  contracting_officers_determination_of_business_size,
  contracting_officers_determination_of_business_size_code,
  community_developed_corporation_owned_firm,
  dot_certified_disadvantage,
  self_certified_small_disadvantaged_business,
  small_disadvantaged_business,
  historically_underutilized_business_zone_hubzone_firm
FROM FY2023_All_Contracts_Full_20241107_7;
DROP TABLE FY2023_All_Contracts_Full_20241107_7;
```

```{python}
file_name = r"C:\Users\cjwfi\Documents\DS2401\final-project-fall-2024-john\col_names.txt"
out_file = r"C:\Users\cjwfi\Documents\DS2401\final-project-fall-2024-john\col_names_2.txt"
col_drop_file = r"C:\Users\cjwfi\Documents\DS2401\final-project-fall-2024-john\col_names_3.txt"
col_list_file = r"C:\Users\cjwfi\Documents\DS2401\final-project-fall-2024-john\col_names_4.txt"

field_int = ['action_date_fiscal_year', 'awarding_agency_code', 'recipient_zip_4_code', 'naics_code']
field_real = ['federal_action_obligation', 'total_dollars_obligated', 'base_and_all_options_value', 'potential_total_value_of_award']
primary_key = 'contract_transaction_unique_key'
main_table_name = 'FY2023_All_Contracts_Full_20241107'
table_count = 7

def field_type_dict(k:list[str]):
    ret = {}
    for s in k:
        type = 'TEXT'
        if s in field_int:
            type = 'INTEGER'
        elif s in field_real:
            type = 'REAL'
        ret[s] = type
    return ret

def write_drops(o_file, keeps, fld_types:dict):
    with open(o_file, 'w') as out_f:
        out_f.write(f'CREATE TABLE {main_table_name}(\n')
        for line in keeps:
            out_f.write(f'\t{line.strip()} {fld_types[line.strip()]},\n')
        out_f.write(f'\tPRIMARY KEY({primary_key})\n')
        out_f.write(');\n')
        for i in range(1,table_count +1):
            out_f.write(f'INSERT INTO {main_table_name} SELECT \n')
            for line in keeps:
                c = '' if line == keeps[-1] else ','
                out_f.write(f'\t{line.strip()}{c}\n')
            out_f.write(f'FROM {main_table_name}_{i};\n')
            out_f.write(f'DROP TABLE {main_table_name}_{i};\n')

def create_keep_list(file):
    keeps = []
    with open(file, 'r') as f:
        for line in f.readlines():
            keeps.append(line.strip())

    # [print(k) for k in keeps]
    return keeps


keep_list = create_keep_list(col_list_file)
field_types = field_type_dict(keep_list)
write_drops(col_drop_file, keep_list, field_types)

```

