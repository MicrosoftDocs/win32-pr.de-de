---
title: Security-Identifier-Attribut
description: Ein eindeutiger Wert der Variablen Länge, mit dem ein Benutzerkonto, ein Gruppenkonto oder eine Anmelde Sitzung identifiziert wird, für die ein ACE gilt.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- AD-Schema für Security-Identifier-Attribut
- SecurityIdentifier-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744529"
---
# <a name="security-identifier-attribute"></a>Security-Identifier-Attribut

Ein eindeutiger Wert der Variablen Länge, mit dem ein Benutzerkonto, ein Gruppenkonto oder eine Anmelde Sitzung identifiziert wird, für die ein ACE gilt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| LDAP-Display-Name | securityIdentifier                   |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID-GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Zeichenfolge (SID)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | False                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | False                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                              |
| Ist indiziert             | False                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





