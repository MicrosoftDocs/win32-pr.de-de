---
title: ms-DS-User-verschlüsselte-Text-Password-Allowed-Attribut
description: Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungs Format speichert.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-verschlüsselte-Text-Password-Allowed\"-Attribut AD-Schema"
- AD-Schema für das Attribut "ms-DS-userencryptedtextpasswordallowed"
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d99ae61566ceec94336fd58951214dfc3255d2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479759"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>ms-DS-User-verschlüsselte-Text-Password-Allowed-Attribut

Gibt an, ob Active Directory das Kennwort im umkehrbaren Verschlüsselungs Format speichert. True, wenn das Kennwort im umkehrbaren Verschlüsselungs Format gespeichert ist. andernfalls false.

> [!Note]  
> Dieses Attribut wird nicht von [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) verwendet und ist nur aus Gründen der Vollständigkeit/Parität mit userAccountControl enthalten. AD LDS speichert keine Kenn Wörter mit umkehrbarer Verschlüsselung, unabhängig vom Wert dieses Attributs für ein bestimmtes Objekt oder die Sicherheitsrichtlinie des Computers in Bezug auf die umkehrbare Verschlüsselung auf dem Computer selbst.

 



| Eingabe | Wert |
|-------------------|--------------------------------------------|
| CN                | ms-DS-Benutzer-verschlüsselt-Text-Kennwort zulässig |
| LDAP-Display-Name | ms-DS-userencryptedtextpasswordallowed     |
| Size              | \-                                         |
| Berechtigung aktualisieren  | \-                                         |
| Aktualisierungshäufigkeit  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID-GUID    | 5a87c7f 2-93c5-454c-a8c5-8cb09613292e       |
| Syntax            | [**Booleschen**](s-boolean.md)               |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Objekt**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Bemerkungen

In Adam ersetzt dieses Attribut das Flag " [**ADS- \_ \_ verschlüsseltes \_ \_ textkennwort \_ zulässig**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " des Attributs " [**userAccountControl**](a-useraccountcontrol.md) ".

 

