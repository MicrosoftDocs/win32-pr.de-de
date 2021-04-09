---
title: MS-SQL-Type-Attribut
description: Der Replikationstyp, der von diesem SQL Server verwendet wird.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-Type-Attributs
- AD-Schema des MS-SQL-Type-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859880"
---
# <a name="ms-sql-type-attribute"></a>MS-SQL-Type-Attribut

Der Replikationstyp, der von diesem SQL Server verwendet wird. Die folgenden Werte sind die möglichen Werte für dieses Attribut.



| Wert        | BESCHREIBUNG                           |
|--------------|---------------------------------------|
| 0<br/> | Transaktionsreplikation.<br/> |
| 1<br/> | Momentaufnahmereplikation.<br/>      |
| 2<br/> | Mergereplikation.<br/>         |



 



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-SQL-Type                                 |
| LDAP-Display-Name | MS-SQL-Type                                 |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Domänen Administrator                        |
| Aktualisierungshäufigkeit  | Wenn die Replikation eingerichtet ist.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-ID-GUID    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | False                                                                                                                               |
| Ist-einwertig       | Richtig                                                                                                                                |
| Ist indiziert             | False                                                                                                                               |
| Im globalen Katalog      | False                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| In verwendete Klassen        | [**MS-SQL-sqlpublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-olapdatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





