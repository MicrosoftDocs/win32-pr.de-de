---
description: Die ODBCDataSource-Tabelle listet die Datenquellen auf, die zur Installation gehören.
ms.assetid: dea28324-e48d-49e8-a4d2-309f7e7cb4b0
title: ODBCDataSource-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43426ba7f2dd1214dc205213aa632558bbc44d81db5e6e32f7f7d66f82d30641
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082720"
---
# <a name="odbcdatasource-table"></a>ODBCDataSource-Tabelle

Die ODBCDataSource-Tabelle listet die Datenquellen auf, die zur Installation gehören.

Die ODBCDataSource-Tabelle enthält die folgenden Spalten.



| Spalte            | Typ                         | Key | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| DataSource        | [Identifier](identifier.md) | J   | N        |
| Komponente\_       | [Identifier](identifier.md) | N   | N        |
| BESCHREIBUNG       | [Text](text.md)             | N   | N        |
| DriverDescription | [Text](text.md)             | N   | N        |
| Registrierung      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DataSource"></span><span id="datasource"></span><span id="DATASOURCE"></span>Datasource
</dt> <dd>

Interner Tokenname für die Datenquelle. Ein Primärschlüssel für die Tabelle.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel in die [Component-Tabelle.](component-table.md)

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Die für diese Datenquelle registrierte Beschreibung. Dieser Wert kann nicht lokalisiert werden. Odbc-Datenquellenbeschreibungen dürfen SQL \_ MAX \_ DSN LENGTH nicht \_ überschreiten.

</dd> <dt>

<span id="DriverDescription"></span><span id="driverdescription"></span><span id="DRIVERDESCRIPTION"></span>DriverDescription
</dt> <dd>

Zugeordneter Treiber, der möglicherweise bereits vorhanden ist. Dieser Wert kann nicht lokalisiert werden.

</dd> <dt>

<span id="Registration"></span><span id="registration"></span><span id="REGISTRATION"></span>Registrierung
</dt> <dd>

Dieses Feld gibt den Typ der Registrierung für die Datenquelle an.



| Konstante                                      | Hexadezimal | Decimal | BESCHREIBUNG                            |
|-----------------------------------------------|-------------|---------|----------------------------------------|
| **msidbODBCDataSourceRegistrationPerMachine** | 0x000       | 0       | Die Datenquelle wird pro Computer registriert. |
| **msidbODBCDataSourceRegistrationPerUser**    | 0x001       | 1       | Die Datenquelle wird pro Benutzer registriert.    |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen InstallODBC](installodbc-action.md) und [RemoveODBC](removeodbc-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE98](ice98.md)  
</dl>

 

 



