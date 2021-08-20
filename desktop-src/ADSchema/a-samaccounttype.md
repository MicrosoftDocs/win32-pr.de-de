---
title: SAM-Account-Type-Attribut
description: Dieses Attribut enthält Informationen zu jedem Kontotypobjekt.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- AD-Schema des SAM-Kontotypattributs
- AD-Schema des sAMAccountType-Attributs
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132532af58eafa4950f049fb08ff7a4235cb49ac2b1f62fc832e308e7ab6d31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118423387"
---
# <a name="sam-account-type-attribute"></a>SAM-Account-Type-Attribut

Dieses Attribut enthält Informationen zu jedem Kontotypobjekt. Sie können eine Liste von Kontotypen auflisten oder die API zum Anzeigen von Informationen verwenden, um eine Liste zu erstellen. Da Computer, normale Benutzerkonten und Vertrauenskonten auch als Benutzerobjekte aufzählt werden können, müssen die Werte für diese Konten ein zusammenhängender Bereich sein.

Die möglichen Werte für dieses Attribut sind die folgenden:

-   SAM \_ DOMAIN \_ OBJECT 0x0
-   SAM \_ GROUP \_ OBJECT 0x10000000
-   SAM \_ NON SECURITY GROUP OBJECT \_ \_ \_ 0X10000001
-   SAM \_ ALIAS \_ OBJECT 0x20000000
-   SAM \_ NON SECURITY ALIAS OBJECT \_ \_ \_ 0x20000001
-   SAM \_ USER \_ OBJECT 0x30000000
-   SAM \_ NORMAL USER ACCOUNT \_ \_ 0X30000000
-   SAM \_ \_ MACHINE-0X30000001
-   SAM \_ TRUST \_ ACCOUNT 0x30000002
-   SAM \_ APP BASIC GROUP \_ \_ 0x40000000
-   SAM \_ APP QUERY GROUP \_ \_ 0X40000001
-   SAM \_ ACCOUNT TYPE MAX \_ \_ 0x7fffffff



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------|
| CN                | SAM-Account-Type                                                |
| Ldap-Anzeigename | sAMAccountType                                                  |
| Size              | \-                                                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                                |
| Updatehäufigkeit  | Dies wird vom Betriebssystem festgelegt, wenn das -Objekt erstellt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-Id-Guid    | 6e7b626c-64f2-11d0-afd2-00c04fd930c9                            |
| Syntax            | [**Enumeration**](s-enumeration.md)                            |



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
| System-Only            | False                                                        |
| Is-Single-Valued       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Is-Single-Valued       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Is-Single-Valued       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist einwertig       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist einwertig       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist einwertig       | True                                                         |
| Ist indiziert             | True                                                         |
| Im globalen Katalog      | True                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



 

 





