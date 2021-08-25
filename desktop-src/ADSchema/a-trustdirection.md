---
title: Trust-Direction-Attribut
description: Die Richtung einer Vertrauensstellung.
ms.assetid: 29ee19c6-a6c5-40e6-ad70-bfa0a16e3a84
ms.tgt_platform: multiple
keywords:
- Trust-Direction AD-Attributschema
- trustDirection-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Direction
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315a52d7bc8a905915d286cea1985348610858c9ae0674e12cda98cb53978cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835490"
---
# <a name="trust-direction-attribute"></a>Trust-Direction-Attribut

Die Richtung einer Vertrauensstellung.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Trust-Direction                      |
| Ldap-Anzeigename | Trustdirection                       |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | Wenn eine neue Vertrauensstellung erstellt wird.         |
| Attribute-Id      | 1.2.840.113556.1.4.132               |
| System-ID-GUID    | bf967a5c-0de6-11d0-a285-00aa003049e2 |
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
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Falsch                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
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
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Ist einwertig       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
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
| System-Only            | Falsch                                                |
| Is-Single-Valued       | Richtig                                                 |
| Ist indiziert             | Falsch                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
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
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
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
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Trusted-Domain**](c-trusteddomain.md)<br/> |



 

 





