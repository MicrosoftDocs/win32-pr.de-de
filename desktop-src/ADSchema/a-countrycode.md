---
title: Country-Code-Attribut
description: Gibt den Länder-/Regionscode für die bevorzugte Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.
ms.assetid: 7011cb76-aa86-4203-bcc4-0136bb11c403
ms.tgt_platform: multiple
keywords:
- AD-Schema für Country-Code-Attribut
- AD-Schema für CountryCode-Attribut
topic_type:
- apiref
api_name:
- Country-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9523a5aab21e81c2b0a5479def8ed8923751daed
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342713"
---
# <a name="country-code-attribute"></a>Country-Code-Attribut

Gibt den Länder-/Regionscode für die bevorzugte Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.



| Eingabe | Wert |
|-------------------|-----------------------------------------|
| CN                | Country-Code                            |
| LDAP-Display-Name | countryCode                             |
| Size              | 2 Bytes                                 |
| Berechtigung aktualisieren  | Konto Besitzer oder Domänen Administrator   |
| Aktualisierungshäufigkeit  | Wenn das Land oder die Region des Benutzers geändert wird. |
| Attribute-Id      | 1.2.840.113556.1.4.25                   |
| System-ID-GUID    | 5F d42471-1262-11D0-a060-00aa006c33ed    |
| Syntax            | [**Enumeration**](s-enumeration.md)    |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | \-                                                                                                                                |
| Range-Upper            | \-                                                                                                                                |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65.535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------|
| Link-ID                | \-                                                             |
| MAPI-Id                | \-                                                             |
| System-Only            | False                                                          |
| Ist-einwertig       | Richtig                                                           |
| Ist indiziert             | False                                                          |
| Im globalen Katalog      | False                                                          |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                   |
| Range-Lower            | 0                                                              |
| Range-Upper            | 65.535                                                          |
| Search-Flags           | 0x00000010                                                     |
| System-Flags           | 0x00000010                                                     |
| In verwendete Klassen        | [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65.535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65.535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65.535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                |
| MAPI-Id                | \-                                                                                                                                |
| System-Only            | False                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                              |
| Ist indiziert             | False                                                                                                                             |
| Im globalen Katalog      | False                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                      |
| Range-Lower            | 0                                                                                                                                 |
| Range-Upper            | 65.535                                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                                        |
| System-Flags           | 0x00000010                                                                                                                        |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



 

 





