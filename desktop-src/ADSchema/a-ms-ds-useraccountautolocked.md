---
title: ms-DS-User-Account-Auto-Locked-Attribut
description: Gibt an, ob das Konto, auf das dieses Attribut verweist, gesperrt wurde.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-User-Account-Auto-Locked-Attributs
- AD-Schema des ms-DS-UserAccountAutoLocked-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1360b9169d5355ef23caf47fa56a283dc4e5267fb603aa08bd0600f126c69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119300300"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>ms-DS-User-Account-Auto-Locked-Attribut

Gibt an, ob das Konto, auf das dieses Attribut verweist, gesperrt wurde. TRUE, wenn das Konto gesperrt ist; andernfalls False.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Auto-Locked       |
| Ldap-Anzeigename | ms-DS-UserAccountAutoLocked          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-Id-Guid    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Syntax            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falsch                                                             |
| Is-Single-Valued       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM ersetzt dieses Attribut das [**ADS \_ UF \_ LOCKOUT-Flag**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) des [**userAccountControl-Attributs.**](a-useraccountcontrol.md)

 

