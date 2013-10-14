PeachQL
=======

Having trouble querying Peachtree or Sage 50 via ODBC? Try this !

	select
		xf$Name as tablename,
		xe$Name as fieldname,
		xf$id as tableid,
		xe$id as fieldid,
		xe$datatype as datatype,
		xe$size as size
	from 
		x$File f
			inner join x$Field e on e.xe$file = f.xf$id
	where 
		tableid in (11,22,33,34,46,38,46,51,52,55,56,58,72,96)
	order by 
		tableid asc, 
		fieldname asc
		
Just a few SQL scripts to help work with Peachtree / Sage 50 databases. ERP / LOL.
