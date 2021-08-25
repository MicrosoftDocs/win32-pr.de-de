---
title: Force-Logoff-Attribut
description: Wird zum Berechnen der Startzeit in SamIGetAccountRestrictions verwendet. Abmeldungszeit minus Abmeldung erzwingen gleich Startzeit.
ms.assetid: 2ce1d5db-52aa-49c5-aef2-ec67122100ed
ms.tgt_platform: multiple
keywords:
- Force-Logoff AD-Attributschema
- forceLogoff-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Force-Logoff
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df1ab9721643edec3e03e91475c74e63dde94dcb982e0a84aad3cdf7c63b806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925850"
---
# <a name="force-logoff-attribute"></a>Force-Logoff-Attribut

Wird zum Berechnen der Startzeit in SamIGetAccountRestrictions verwendet. Abmeldungszeit minus Abmeldung erzwingen gleich Startzeit.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Force-Logoff                         |
| Ldap-Anzeigename | forceLogoff                          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.39                |
| System-ID-GUID    | bf967977-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                       |
| MAPI-Id                | \-                                                                                                       |
| System-Only            | Falsch                                                                                                    |
| Ist einwertig       | Richtig                                                                                                     |
| Ist indiziert             | Falsch                                                                                                    |
| Im globalen Katalog      | Falsch                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                             |
| Range-Lower            | \-                                                                                                       |
| Range-Upper            | \-                                                                                                       |
| Search-Flags           | 0x00000000                                                                                               |
| System-Flags           | 0x00000010                                                                                               |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





