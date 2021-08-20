---
title: Max-Renew-Age-Attribut
description: Dieses Attribut bestimmt den Zeitraum in Tagen, in dem das Ticketgewährungsticket (Ticket Granting Ticket, TGT) eines Benutzers für die Kerberos-Authentifizierung erneuert werden kann. Die Standardeinstellung beträgt 7 Tage im Standarddomänen-Gruppenrichtlinie-Objekt (GPO).
ms.assetid: 9e4023d1-b88b-44c9-802b-03387614211d
ms.tgt_platform: multiple
keywords:
- AD-Schema des Max-Renew-Age-Attributs
- MAXRenewAge-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Max-Renew-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982b3b781ecfaea05352ac8efd41e023295da65a1251df0ade51a9bd6e4953a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017060"
---
# <a name="max-renew-age-attribute"></a>Max-Renew-Age-Attribut

Dieses Attribut bestimmt den Zeitraum in Tagen, in dem das Ticketgewährungsticket (Ticket Granting Ticket, TGT) eines Benutzers für die Kerberos-Authentifizierung erneuert werden kann. Die Standardeinstellung beträgt 7 Tage im Standarddomänen-Gruppenrichtlinie-Objekt (GPO).



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Max-Renew-Age                        |
| Ldap-Anzeigename | maxRenewAge                          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.75                |
| System-ID-GUID    | bf9679bc-0de6-11d0-a285-00aa003049e2 |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | Richtig                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
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
| System-Only            | Falsch                                              |
| Ist einwertig       | True                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



 

 





