---
title: Pwd-History-Length-Attribut
description: Die Anzahl der zu speichernden alten Kennwörter.
ms.assetid: 6440620d-9e77-411a-ab96-f8e979262bec
ms.tgt_platform: multiple
keywords:
- Pwd-History-Length-Attribut AD-Schema
- pwdHistoryLength-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Pwd-History-Length
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9c2c5011b2c497e8b6ed69015dd7dd16fbd2bf979d199674dd6ccbb2a67b81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960099"
---
# <a name="pwd-history-length-attribute"></a>Pwd-History-Length-Attribut

Die Anzahl der zu speichernden alten Kennwörter.



| Eingabe | Wert |
|-------------------|------------------------------------------|
| CN                | Pwd-History-Length                       |
| Ldap-Anzeigename | pwdHistoryLength                         |
| Size              | 4 Bytes                                  |
| Aktualisieren von Berechtigungen  | Domänenadministrator                     |
| Updatehäufigkeit  | Wenn die Kontorichtlinie geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.95                    |
| System-Id-Guid    | bf967a09-0de6-11d0-a285-00aa003049e2     |
| Syntax            | [**Enumeration**](s-enumeration.md)     |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | 0                                                                                                                                                     |
| Range-Upper            | 65.535                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





