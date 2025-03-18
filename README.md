1)
Select count(*) from invoice   -- 0 rows --
WHERE invoice_id is null
AND customer_id is null
AND invoice_date is null
AND billing_address is null
AND billing_city is null
AND billing_state is null
AND billing_country is null
AND billingpostal_code is null
AND total is null;

2)
Select invoice_id, total as eski_total, total*2 as yeni_total from invoice order by yeni_total desc;

3)
Select invoice_id, CONCAT(substring(billing_address, 1, 3),'***** ', substring( billing_address, length(billing_address) -3 , 4 ))as Acık_adres from invoice
where invoice_date between '2013-08-01'and '2013-08-31';



