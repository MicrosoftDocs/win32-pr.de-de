---
title: Street-Address-Attribut
description: Die Adresse der Straße.
ms.assetid: 09a94b72-14cb-4d4d-b885-4015f65db139
ms.tgt_platform: multiple
keywords:
- AD-Schema für Street-Address-Attribut
- AD-Schema für Straße
topic_type:
- apiref
api_name:
- Street-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6c109df2af4eaf6fd82acc88bb0cf14e2d2a2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957576"
---
# <a name="street-address-attribute"></a>Street-Address-Attribut

Die Adresse der Straße.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Street-Address                                                                   |
| LDAP-Display-Name | street                                                                           |
| Size              | \-                                                                               |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren. |
| Aktualisierungshäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.9                                                                          |
| System-ID-GUID    | bf967a3a-0de6-11d0-a285-00aa003049e2                                             |
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
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                         |
| MAPI-Id                | 0x813a                                                                                                                                                     |
| System-Only            | False                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813a                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





