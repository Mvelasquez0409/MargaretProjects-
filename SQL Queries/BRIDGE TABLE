SELECT

    --fs.SalesOrderNumber AS InvoiceNumber,
    --fs.SalesOrderLineNumber AS InvoiceLineNumber,
    dsr.SalesReasonReasonType AS SalesReason,
    SUM(fs.SalesAmount) AS SalesAmount

FROM FactInternetSales AS fs
    INNER JOIN FactInternetSalesReason AS fsr
    ON fs.SalesOrderNumber = fsr.SalesOrderNumber AND fs.SalesOrderLineNumber = fsr.SalesOrderLineNumber
    INNER JOIN DimSalesReason dsr
    ON fsr.SalesReasonKey = dsr.SalesReasonKey

--WHERE fs.SalesOrderNumber = N'SO51178'

GROUP BY dsr.SalesReasonReasonType
