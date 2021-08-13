---
title: ms-DS-User-Encrypted-Text-Password-Allowed-Attribut
description: Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungsformat speichert.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- ms-DS-User-Encrypted-Text-Password-Allowed attribute AD Schema
- ms-DS-UserEncryptedTextPasswordAllowed-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687001"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>ms-DS-User-Encrypted-Text-Password-Allowed-Attribut

Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungsformat speichert. TRUE, wenn das Kennwort im umkehrbaren Verschlüsselungsformat gespeichert ist; Andernfalls False.

> [!Note]  
> Dieses Attribut wird nicht von [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) verwendet und ist nur für Vollständigkeit/Parität mit userAccountControl enthalten. AD LDS speichert Kennwörter nicht mit umkehrbarer Verschlüsselung, unabhängig vom Wert dieses Attributs für ein bestimmtes Objekt oder der Computersicherheitsrichtlinie für umkehrbare Verschlüsselung auf dem Computer selbst.

 



| Eingabe | Wert |
|-------------------|--------------------------------------------|
| CN                | ms-DS-User-Encrypted-Text-Password-Allowed |
| Ldap-Anzeigename | ms-DS-UserEncryptedTextPasswordAllowed     |
| Size              | \-                                         |
| Aktualisieren von Berechtigungen  | \-                                         |
| Updatehäufigkeit  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Syntax            | [**Boolean**](s-boolean.md)               |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM ersetzt dieses Attribut das [**ADS \_ UF \_ ENCRYPTED TEXT \_ PASSWORD \_ \_ ALLOWED-Flag**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) des [**userAccountControl-Attributs.**](a-useraccountcontrol.md)

 

