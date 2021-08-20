---
title: MS-SQL-RegisteredOwner-Attribut
description: Der registrierte Besitzer für die aktuelle Instanz SQL Server.
ms.assetid: d07712e8-021d-40db-91ba-0fef7e89bb0f
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-SQL-RegisteredOwner-Attributs
- AD-Schema des mS-SQL-RegisteredOwner-Attributs
topic_type:
- apiref
api_name:
- MS-SQL-RegisteredOwner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e11fd5b7b3157d64ebe13cdb57e0133eaaf2ac4a0cd5cfcff0dae9c970840eb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118016196"
---
# <a name="ms-sql-registeredowner-attribute"></a>MS-SQL-RegisteredOwner-Attribut

Der registrierte Besitzer für die aktuelle Instanz SQL Server.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-SQL-RegisteredOwner                      |
| Ldap-Anzeigename | mS-SQL-RegisteredOwner                      |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator                        |
| Updatehäufigkeit  | Beim Systemsetup.                            |
| Attribute-Id      | 1.2.840.113556.1.4.1364                     |
| System-Id-Guid    | 48fd44ea-ccee-11d2-9993-0000f87a57d4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Is-Single-Valued       | Richtig                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Ist einwertig       | Richtig                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Ist einwertig       | True                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                    |
| MAPI-Id                | \-                                                                                                                    |
| System-Only            | Falsch                                                                                                                 |
| Ist einwertig       | True                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                          |
| Range-Lower            | \-                                                                                                                    |
| Range-Upper            | \-                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                            |
| System-Flags           | 0x00000010                                                                                                            |
| In verwendete Klassen        | [**MS-SQL-SQLServer**](c-ms-sql-sqlserver.md)<br/> [**MS-SQL-OLAPServer**](c-ms-sql-olapserver.md)<br/> |



 

 





