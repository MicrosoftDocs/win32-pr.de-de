---
title: Max-Ticket-Age-Attribut
description: Dieses Attribut bestimmt die maximale Zeitdauer in Stunden, die das Ticket-Granting Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- AD-Schema des Max-Ticket-Age-Attributs
- maxTicketAge-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c876bbab2b60d655464129d0a59aeda110f78d8e2514866a3bcf28a859cb3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301010"
---
# <a name="max-ticket-age-attribute"></a>Max-Ticket-Age-Attribut

Dieses Attribut bestimmt die maximale Zeitdauer in Stunden, die das Ticket-Granting Ticket (TGT) eines Benutzers für die Kerberos-Authentifizierung verwendet werden kann. Wenn das TGT eines Benutzers abläuft, muss ein neues angefordert werden, oder das vorhandene muss erneuert werden. Standardmäßig ist diese Einstellung im Standarddomänenobjekt (GPO) Gruppenrichtlinie 10 Stunden festgelegt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Max-Ticket-Age                       |
| Ldap-Anzeigename | maxTicketAge                         |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-Id-Guid    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Is-Single-Valued       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Is-Single-Valued       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Is-Single-Valued       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------|
| Link-ID                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | False                                              |
| Im globalen Katalog      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



 

 





