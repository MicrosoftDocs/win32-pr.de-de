---
title: Security-Identifier-Attribut
description: Ein eindeutiger Wert variabler Länge, der verwendet wird, um ein Benutzerkonto, ein Gruppenkonto oder eine Anmeldesitzung zu identifizieren, für die ein ACE gilt.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Security-Identifier AD-Attributschema
- securityIdentifier-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f15449127dd11e7e0ebfef9f63d8e79470ed662377cbdd1929ed072b2502dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836870"
---
# <a name="security-identifier-attribute"></a>Security-Identifier-Attribut

Ein eindeutiger Wert variabler Länge, der verwendet wird, um ein Benutzerkonto, ein Gruppenkonto oder eine Anmeldesitzung zu identifizieren, für die ein ACE gilt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| Ldap-Anzeigename | securityIdentifier                   |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID-GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Ist einwertig       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Falsch                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Ist einwertig       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Ist einwertig       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Trusted-Domain**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falsch                                                                                                             |
| Is-Single-Valued       | Richtig                                                                                                              |
| Ist indiziert             | Falsch                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Trusted-Domain**](c-trusteddomain.md)<br/> |



 

 





