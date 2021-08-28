---
title: Nachname-Attribut
description: Dieses Attribut enthält die Familie oder den Nachnamen eines Benutzers.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Nachnamenattribut AD-Schema
- AD-Schema des sn-Attributs
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655557c23475dbc2d7f2e92fb48f5f71a8e818954bff83f5a47bb2470a26ca20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836190"
---
# <a name="surname-attribute"></a>Nachname-Attribut

Dieses Attribut enthält die Familie oder den Nachnamen eines Benutzers.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Surname                                                                          |
| Ldap-Anzeigename | sn                                                                               |
| Size              | \-                                                                               |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt basierend auf der Sicherheit des zu erstellenden Objekts aktualisieren. |
| Updatehäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.4                                                                          |
| System-Id-Guid    | bf967a41-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|---------------------------------------|
| Link-ID                | \-                                    |
| MAPI-Id                | 0x3A11                                |
| System-Only            | Falsch                                 |
| Is-Single-Valued       | Richtig                                  |
| Ist indiziert             | Richtig                                  |
| Im globalen Katalog      | Richtig                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 64                                    |
| Search-Flags           | 0x00000005                            |
| System-Flags           | 0x00000010                            |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falsch                                                                                         |
| Is-Single-Valued       | Richtig                                                                                          |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falsch                                                                                         |
| Is-Single-Valued       | Richtig                                                                                          |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falsch                                                                                         |
| Ist einwertig       | Richtig                                                                                          |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falsch                                                                                         |
| Ist einwertig       | Richtig                                                                                          |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                            |
| MAPI-Id                | 0x3A11                                                                                        |
| System-Only            | Falsch                                                                                         |
| Ist einwertig       | Richtig                                                                                          |
| Ist indiziert             | Richtig                                                                                          |
| Im globalen Katalog      | Richtig                                                                                          |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                  |
| Range-Lower            | 1                                                                                             |
| Range-Upper            | 64                                                                                            |
| Search-Flags           | 0x00000005                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| In verwendete Klassen        | [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





