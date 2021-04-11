---
title: State-oder Province-Name-Attribut
description: Der Name des Zustands oder der Provinz eines Benutzers.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- AD-Schema für State-oder Province-Name-Attribut
- St-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677daf6d72c63ffd08cc1ac8540e4ba03c3af792
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041063"
---
# <a name="state-or-province-name-attribute"></a>State-oder Province-Name-Attribut

Der Name des Zustands oder der Provinz eines Benutzers.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | State-or-Province-Name                                                           |
| LDAP-Display-Name | st                                                                               |
| Size              | \-                                                                               |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren. |
| Aktualisierungshäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-ID-GUID    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3a28                                                                                                                                                     |
| System-Only            | False                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3a28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



 

 





