# SQL_Projects

-- Q1.
SELECT 
	staff.first_name,
    staff.last_name,
    staff.store_id,
    address.address,
	address.district,
    city.city,
    country.country
FROM 
	store 
	LEFT JOIN staff ON store.manager_staff_id = staff.staff_id
	LEFT JOIN address ON store.address_id = address.address_id
	LEFT JOIN city ON address.city_id = city.city_id
	LEFT JOIN country ON city.country_id = country.country_id;



