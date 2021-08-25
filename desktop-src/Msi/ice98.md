---
description: ICE98 überprüft das Beschreibungsfeld der ODBCDataSource-Tabelle für eine ODBC-Datenquelle. Sie verwendet die SQLValidDSN-Funktion, um zu überprüfen, ob nur gültige Zeichen verwendet werden und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894690"
---
# <a name="ice98"></a>ICE98

ICE98 überprüft das Beschreibungsfeld der [ODBCDataSource-Tabelle](odbcdatasource-table.md) für eine ODBC-Datenquelle. Sie verwendet die **SQLValidDSN-Funktion,** um zu überprüfen, ob nur gültige Zeichen verwendet werden und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.

## <a name="result"></a>Ergebnis

ICE98 gibt die folgenden Warnungen aus.



| ICE98-Warnung                    | BESCHREIBUNG                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Datenquellenname ist ungültig. | Der Wert in der Spalte Beschreibung der [ODBCDataSource-Tabelle](odbcdatasource-table.md) enthält entweder ungültige Zeichen oder ist zu lang, was bedeutet, dass er die SQL \_ MAX \_ DSN \_ LENGTH von 32 überschreitet. |



 

## <a name="example"></a>Beispiel

ICE98 meldet die folgenden Warnungen für das Beispiel:

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[ODBCDataSource-Tabelle](odbcdatasource-table.md) (partiell)



| DataSource | BESCHREIBUNG                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> <dt>

[ODBCDataSource-Tabelle](odbcdatasource-table.md)
</dt> </dl>

 

 



