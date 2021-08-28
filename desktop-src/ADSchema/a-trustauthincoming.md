---
title: Trust-Auth-Incoming-Attribut
description: Authentifizierungsinformationen für den eingehenden Teil einer Vertrauensstellung.
ms.assetid: 15d079f8-a77c-4baf-bb60-1af7a8e8da25
ms.tgt_platform: multiple
keywords:
- Trust-Auth-Incoming-Attribut-AD-Schema
- trustAuthIncoming-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac7d9c6d56628d95564fe5bb4e33e08df38056f62606cfda6f0699e0af06041
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835662"
---
# <a name="trust-auth-incoming-attribute"></a>Trust-Auth-Incoming-Attribut

Authentifizierungsinformationen für den eingehenden Teil einer Vertrauensstellung.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Trust-Auth-Incoming                                   |
| Ldap-Anzeigename | trustAuthIncoming                                     |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.129                                |
| System-ID-GUID    | bf967a59-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 32767                                                |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



 

 





