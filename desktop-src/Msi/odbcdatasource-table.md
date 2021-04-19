---
description: In der Tabelle ODBCDatasource sind die Datenquellen aufgelistet, die zur Installation gehören.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: ODBCDatasource-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819eecc671c75fa11db6e4a2706a511c2758ad00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353132"
---
# <a name="odbcdatasource-table"></a>ODBCDatasource-Tabelle

In der Tabelle ODBCDatasource sind die Datenquellen aufgelistet, die zur Installation gehören.

Die ODBCDatasource-Tabelle weist die folgenden Spalten auf.



| Spalte            | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Bezeichner](identifier.md) | J   | N        |
| Komponente\_       | [Bezeichner](identifier.md) | N   | N        |
| BESCHREIBUNG       | [Text](text.md)             | N   | N        |
| Driverdescription | [Text](text.md)             | N   | N        |
| Registrierung      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>DataSource
</dt> <dd>

Interner Tokenname für die Datenquelle. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel in der [Komponenten Tabelle](component-table.md).

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die Beschreibung, die für diese Datenquelle registriert ist. Dieser Wert kann nicht lokalisiert werden. ODBC-Datenquellen Beschreibungen dürfen die maximale SQL-DSN-Länge nicht überschreiten \_ \_ \_ .

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>Driverdescription
</dt> <dd>

Zugeordneter Treiber, der möglicherweise bereits vorhanden ist. Dieser Wert kann nicht lokalisiert werden.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Nummern
</dt> <dd>

Dieses Feld gibt den Registrierungstyp für die Datenquelle an.



| Konstante                                      | Hexadezimal | Decimal | BESCHREIBUNG                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbodbcdatasourceregistrationpermachine** | 0x000       | 0       | Die Datenquelle wird pro Computer registriert. |
| **msidbodbcdatasourceregistrationperuser**    | 0x001       | 1       | Die Datenquelle wird pro Benutzer registriert.    |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Informationen in dieser Tabelle werden durch die [installlodbc](installodbc-action.md) -und [removeodbc](removeodbc-action.md) -Aktionen in [*Sequenz Tabellen*](s-gly.md) verarbeitet. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



