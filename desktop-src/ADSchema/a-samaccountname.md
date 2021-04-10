---
title: Sam-Account-Name-Attribut
description: Der Anmelde Name, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. b. Windows NT 4,0, Windows 95, Windows 98 und LAN-Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- "\"Sam-Account-Name\"-Attribut AD-Schema"
- sAMAccountName-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859764"
---
# <a name="sam-account-name-attribute"></a>Sam-Account-Name-Attribut

Der Anmelde Name, der zur Unterstützung von Clients und Servern verwendet wird, auf denen frühere Versionen des Betriebssystems ausgeführt werden, z. b. Windows NT 4,0, Windows 95, Windows 98 und LAN-Manager.

Dieses Attribut darf maximal 20 Zeichen lang sein, um frühere Clients zu unterstützen, und darf keines der folgenden Zeichen enthalten:

-   "/ \\ \[ \] : ; \| = , + \* ? < >



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| CN                | Sam-Account-Name                                                                         |
| LDAP-Display-Name | sAMAccountName                                                                           |
| Size              | maximal 20 Zeichen.                                                                   |
| Berechtigung aktualisieren  | Domänen Administrator                                                                     |
| Aktualisierungshäufigkeit  | Dieser Wert sollte beim Erstellen des Kontodaten Satzes zugewiesen werden und sollte nicht geändert werden. |
| Attribute-Id      | 1.2.840.113556.1.4.221                                                                   |
| System-ID-GUID    | 3e0abf D0-126a-11D0-a060-00aa006c33ed                                                     |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                              |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 256                                                          |
| Search-Flags           | 0x0000000d                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



 

 





