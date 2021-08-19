---
title: ms-DS-User-Dont-Expire-Password-Attribut
description: Gibt an, ob das Kennwort für das Konto abläuft, auf das dieses Attribut verweist.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-User-Dont-Expire-Password-Attributs
- AD-Schema des msDS-UserDontExpirePassword-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425430"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>ms-DS-User-Dont-Expire-Password-Attribut

Gibt an, ob das Kennwort für das Konto abläuft, auf das dieses Attribut verweist. TRUE, wenn das Kennwort nicht abläuft; andernfalls False.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Dont-Expire-Password      |
| Ldap-Anzeigename | msDS-UserDontExpirePassword          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-Id-Guid    | 8788193a-2925-43d9-a221-bb7fff397675 |
| Syntax            | [**Boolesch**](s-boolean.md)         |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Is-Single-Valued       | True                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM ersetzt dieses Attribut das [**ADS \_ UF \_ DONT \_ EXPIRE \_ PASSWD-Flag**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) des [**userAccountControl-Attributs.**](a-useraccountcontrol.md)

 

