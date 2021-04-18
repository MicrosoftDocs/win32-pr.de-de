---
title: Registered-Address-Attribut
description: Gibt einen mnetmonischen für eine Adresse an, die einem Objekt an einem bestimmten Ort zugeordnet ist. Der mnetmonic ist in dem Land bzw. der Region registriert, in dem sich die Stadt befindet, und wird bei der Bereitstellung des öffentlichen Telegramm Dienstanbieter verwendet.
ms.assetid: 5bc1eecd-0263-46da-a842-75ee94f77b58
ms.tgt_platform: multiple
keywords:
- AD-Schema für Registered-Address-Attribut
- registeredaddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Registered-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a24093e8ebfa0edd5a2e2101f6da86cd6cd19d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106340043"
---
# <a name="registered-address-attribute"></a>Registered-Address-Attribut

Gibt einen mnetmonischen für eine Adresse an, die einem Objekt an einem bestimmten Ort zugeordnet ist. Der mnetmonic ist in dem Land bzw. der Region registriert, in dem sich die Stadt befindet, und wird bei der Bereitstellung des öffentlichen Telegramm Dienstanbieter verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Registered-Address                                    |
| LDAP-Display-Name | registeredaddress                                     |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | \-                                                    |
| Aktualisierungshäufigkeit  | \-                                                    |
| Attribute-Id      | 2.5.4.26                                              |
| System-ID-GUID    | bf967a10-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x8119                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | False                                                                                                            |
| Ist indiziert             | False                                                                                                            |
| Im globalen Katalog      | False                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000000                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





