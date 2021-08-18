---
title: Trust-Posix-Offset-Attribut
description: Der POSIX-Offset (Portable Operating System Interface) für die vertrauenswürdige Domäne.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- AD-Schema des Trust-Posix-Offset-Attributs
- trustPosixOffset-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f4529c2f3aeef1098d444501a87ed3e45ec39fb2ca6311f9cf017762f091c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022018"
---
# <a name="trust-posix-offset-attribute"></a>Trust-Posix-Offset-Attribut

Der POSIX-Offset (Portable Operating System Interface) für die vertrauenswürdige Domäne.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Trust-Posix-Offset                   |
| Ldap-Anzeigename | trustPosixOffset                     |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | Wenn eine neue Vertrauensstellung erstellt wird.         |
| Attribute-Id      | 1.2.840.113556.1.4.134               |
| System-Id-Guid    | bf967a5e-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





