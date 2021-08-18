---
title: SAM-Account-Name-Attribut
description: Der Anmeldename, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. B. Windows NT 4.0, Windows 95, Windows 98 und LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- AD-Schema des SAM-Account-Name-Attributs
- AD-Schema des sAMAccountName-Attributs
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74aa558f63c2e1822f1435cdafd6290755b92b4d5e34c329d8472693f37185d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022228"
---
# <a name="sam-account-name-attribute"></a>SAM-Account-Name-Attribut

Der Anmeldename, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. B. Windows NT 4.0, Windows 95, Windows 98 und LAN Manager.

Dieses Attribut muss mindestens 20 Zeichen lang sein, um frühere Clients zu unterstützen, und darf keines dieser Zeichen enthalten:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | SAM-Account-Name                                                                         |
| Ldap-Anzeigename | sAMAccountName                                                                           |
| Size              | 20 Zeichen oder weniger.                                                                   |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                                                     |
| Updatehäufigkeit  | Dieser Wert sollte zugewiesen werden, wenn der Kontodatensatz erstellt wird, und sollte sich nicht ändern. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-Id-Guid    | 3e0abfd0-126a-11d0-a060-00aa006c33ed                                                     |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000D                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



 

 





