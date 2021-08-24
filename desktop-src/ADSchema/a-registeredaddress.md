---
title: Registered-Address-Attribut
description: Gibt ein Mnemonic für eine Adresse an, die einem Objekt an einem bestimmten Ort zugeordnet ist. Das Mnemonic wird in dem Land/der Region registriert, in dem bzw. der sich die Stadt befindet, und wird bei der Bereitstellung des öffentlichen Telegram-Diensts verwendet.
ms.assetid: 5bc1eecd-0263-46da-a842-75ee94f77b58
ms.tgt_platform: multiple
keywords:
- Registered-Address AD-Attributschema
- registeredAddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Registered-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31dc42db9a492ee460b46c62f666797291526ca89c6b32f3abb1dd887803b9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837450"
---
# <a name="registered-address-attribute"></a>Registered-Address-Attribut

Gibt ein Mnemonic für eine Adresse an, die einem Objekt an einem bestimmten Ort zugeordnet ist. Das Mnemonic wird in dem Land/der Region registriert, in dem bzw. der sich die Stadt befindet, und wird bei der Bereitstellung des öffentlichen Telegram-Diensts verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Registered-Address                                    |
| Ldap-Anzeigename | registeredAddress                                     |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 2.5.4.26                                              |
| System-ID-GUID    | bf967a10-0de6-11d0-a285-00aa003049e2                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x8119                                                                                                           |
| System-Only            | Falsch                                                                                                            |
| Ist einwertig       | Falsch                                                                                                            |
| Ist indiziert             | Falsch                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000000                                                                                                       |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8119                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





