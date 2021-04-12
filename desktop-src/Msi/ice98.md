---
description: ICE98 überprüft das Beschreibungsfeld der ODBCDatasource-Tabelle für eine ODBC-Datenquelle. Er verwendet die sqlvaliddsn-Funktion, um zu überprüfen, ob nur gültige Zeichen verwendet werden, und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216568"
---
# <a name="ice98"></a>ICE98

ICE98 überprüft das Beschreibungsfeld der [ODBCDatasource-Tabelle](odbcdatasource-table.md) für eine ODBC-Datenquelle. Er verwendet die **sqlvaliddsn** -Funktion, um zu überprüfen, ob nur gültige Zeichen verwendet werden, und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.

## <a name="result"></a>Ergebnis

ICE98 gibt die folgenden Warnungen aus.



| ICE98-Warnung                    | BESCHREIBUNG                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Datenquellen Name ist ungültig. | Der Wert in der Spalte "Beschreibung" der [Tabelle "ODBCDatasource](odbcdatasource-table.md) " enthält entweder ungültige Zeichen oder ist zu lang. Dies bedeutet, dass die maximale SQL- \_ \_ DSN- \_ Länge von 32 überschritten wird. |



 

## <a name="example"></a>Beispiel

ICE98 meldet die folgenden Warnungen für das Beispiel:

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[ODBCDatasource-Tabelle](odbcdatasource-table.md) (partiell)



| DataSource | BESCHREIBUNG                      |
|------------|----------------------------------|
| Badchar    | !                                |
| Toolong    | <String of length > 32> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> <dt>

[ODBCDatasource-Tabelle](odbcdatasource-table.md)
</dt> </dl>

 

 



