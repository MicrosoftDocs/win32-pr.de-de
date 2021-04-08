---
title: Max-Ticket-Age-Attribut
description: Dieses Attribut bestimmt den maximalen Zeitraum (in Stunden), den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- "\"Max-Ticket-Age\"-Attribut AD-Schema"
- Schema des maxticketage-Attributs AD
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744345"
---
# <a name="max-ticket-age-attribute"></a>Max-Ticket-Age-Attribut

Dieses Attribut bestimmt den maximalen Zeitraum (in Stunden), den das Ticket Erteilungs Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann. Wenn das TGT eines Benutzers abläuft, muss ein neues angefordert werden, oder das vorhandene muss erneuert werden. Standardmäßig ist diese Einstellung im Standard-Domänen Gruppenrichtlinie Objekt (GPO) auf 10 Stunden festgelegt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Max-Ticket-Age                       |
| LDAP-Display-Name | maxticketage                         |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID-GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist-einwertig       | Richtig                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> |



 

 





