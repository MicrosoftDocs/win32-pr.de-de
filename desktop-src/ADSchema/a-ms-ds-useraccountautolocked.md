---
title: ms-DS-User-Account-Auto-Locked-Attribut
description: Gibt an, ob das Konto, auf das dieses Attribut verweist, gesperrt wurde.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-Account-Auto-Locked\"-Attribut AD-Schema"
- AD-Schema des ms-DS-useraccountautolocked-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104041096"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms-DS-User-Account-Auto-Locked-Attribut

Gibt an, ob das Konto, auf das dieses Attribut verweist, gesperrt wurde. True, wenn das Konto gesperrt ist. andernfalls false.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Benutzer-Konto-automatisch gesperrt       |
| LDAP-Display-Name | ms-DS-useraccountautolocked          |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID-GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Syntax            | [**Booleschen**](s-boolean.md)         |



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
| System-Flags           | 0x00000014                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Objekt**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Bemerkungen

In Adam ersetzt dieses Attribut das [**ADS- \_ Lock- \_ Lock**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) -Flag des [**userAccountControl**](a-useraccountcontrol.md) -Attributs.

 

