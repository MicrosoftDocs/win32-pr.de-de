---
title: Code-Page-Attribut
description: Gibt die Codepage für die Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Code-Page AD-Attributschema
- CODEPAGE-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff90ba0413288ff09c5793cf582a64d88e1de32ac4a3eeaba3b6ae688bf6f8eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442710"
---
# <a name="code-page-attribute"></a>Code-Page-Attribut

Gibt die Codepage für die Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Code-Page                                             |
| Ldap-Anzeigename | Codepage                                              |
| Size              | 4 Bytes                                               |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                  |
| Updatehäufigkeit  | Wenn der Benutzer die Standardsprache ändern möchte. |
| Attribute-Id      | 1.2.840.113556.1.4.16                                 |
| System-ID-GUID    | bf967938-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Enumeration**](s-enumeration.md)                  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65.535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65.535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65.535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65.535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65.535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





