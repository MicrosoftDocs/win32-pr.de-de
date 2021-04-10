---
title: Ursprüngliches Authentifizierungs Attribut
description: Enthält Informationen über eine anfängliche ausgehende Authentifizierung, die vom Authentifizierungsserver für diese Domäne an den Client gesendet wurde, der die Authentifizierung angefordert hat.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- AD-Schema für das anfängliche auth-ausgehende Attribut
- AD-Schema des initialauthoutgoing-Attributs
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107043"
---
# <a name="initial-auth-outgoing-attribute"></a>Ursprüngliches Authentifizierungs Attribut

Enthält Informationen über eine anfängliche ausgehende Authentifizierung, die vom Authentifizierungsserver für diese Domäne an den Client gesendet wurde, der die Authentifizierung angefordert hat. Der Server, der dieses Attribut verwendet, empfängt die Autorisierung vom Authentifizierungsserver und sendet Sie an den Client.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Anfängliche Authentifizierung: ausgehend                       |
| LDAP-Display-Name | initialauthoutgoing                         |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.540                      |
| System-ID-GUID    | 52458024-ca6a-11D0-affinf-0000f 80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





