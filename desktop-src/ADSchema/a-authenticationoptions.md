---
title: Authentication-Options-Attribut
description: Die Authentifizierungsoptionen, die in ADSI zum Binden an Verzeichnisdienstobjekte verwendet werden.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Authentication-Options AD-Schema des Attributs
- authenticationOptions-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 220438034793c4cae72ab730e8c9116edff69a0524c1dc135185da3ff8b6af73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443010"
---
# <a name="authentication-options-attribute"></a>Authentication-Options-Attribut

Die Authentifizierungsoptionen, die in ADSI zum Binden an Verzeichnisdienstobjekte verwendet werden.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Authentication-Options                                                                                                                                                                                                                                                       |
| Ldap-Anzeigename | authenticationOptions                                                                                                                                                                                                                                                        |
| Size              | 4 Bytes. In IADS.h definierte Werte: ADS SECURE AUTHENTICATION 0x1, ADS USE ENCRYPTION 0X2, ADS \_ USE \_ SSL \_ \_ \_ \_ 0x2, ADS \_ READONLY \_ SERVER 0X4, ADS PROMPT CREDENTIALS \_ \_ 0x8, ADS NO AUTHENTICATION \_ 0x10, ADS FAST BIND 0x20, ADS USE SIGNING \_ \_ \_ \_ \_ 0x40, ADS USE ADS USE \_ ADS USE ADS \_ 0X80 |
| Aktualisieren von Berechtigungen  | \-                                                                                                                                                                                                                                                                           |
| Updatehäufigkeit  | \-                                                                                                                                                                                                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.4.11                                                                                                                                                                                                                                                        |
| System-Id-Guid    | bf967928-0de6-11d0-a285-00aa003049e2                                                                                                                                                                                                                                         |
| Syntax            | [**Enumeration**](s-enumeration.md)                                                                                                                                                                                                                                         |



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
| Is-Single-Valued       | Richtig                                               |
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
| Is-Single-Valued       | Richtig                                               |
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
| Is-Single-Valued       | Richtig                                               |
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
| Ist einwertig       | Richtig                                               |
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
| Ist einwertig       | Richtig                                               |
| Ist indiziert             | Falsch                                              |
| Im globalen Katalog      | Falsch                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> |



 

 





