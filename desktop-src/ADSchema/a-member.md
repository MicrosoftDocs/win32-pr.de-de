---
title: Member-Attribut
description: Die Liste der Benutzer, die zur Gruppe gehören.
ms.assetid: 0f5e249e-1fa1-4191-90e6-94c0b657b7fc
ms.tgt_platform: multiple
keywords:
- AD-Schema des Mitglieds Attributs
- AD-Schema des Mitglieds Attributs
topic_type:
- apiref
api_name:
- Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c237c7cb7b41ae73bcbdff5a13f6cb34f546449b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344735"
---
# <a name="member-attribute"></a>Member-Attribut

Die Liste der Benutzer, die zur Gruppe gehören.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Member                                                |
| LDAP-Display-Name | Member                                                |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | Domänen Administrator                                  |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn ein Benutzer einer Gruppe hinzugefügt oder daraus entfernt wird. |
| Attribute-Id      | 2.5.4.31                                              |
| System-ID-GUID    | bf9679c0-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)               |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                       |
| MAPI-Id                | 0x8009                                                                                  |
| System-Only            | False                                                                                   |
| Ist-einwertig       | False                                                                                   |
| Ist indiziert             | False                                                                                   |
| Im globalen Katalog      | Richtig                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                            |
| Range-Lower            | \-                                                                                      |
| Range-Upper            | \-                                                                                      |
| Search-Flags           | 0x00000000                                                                              |
| System-Flags           | 0x00000012                                                                              |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Gruppe**](c-msmq-group.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | 2                                   |
| MAPI-Id                | 0x8009                              |
| System-Only            | False                               |
| Ist-einwertig       | False                               |
| Ist indiziert             | False                               |
| Im globalen Katalog      | Richtig                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000012                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Gruppe**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Gruppe**](c-msmq-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Gruppe**](c-msmq-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 2                                                                                                                                     |
| MAPI-Id                | 0x8009                                                                                                                                |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | False                                                                                                                                 |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | \-                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000012                                                                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Gruppe von Namen**](c-groupofnames.md)<br/> [**MSMQ-Gruppe**](c-msmq-group.md)<br/> |



 

 





