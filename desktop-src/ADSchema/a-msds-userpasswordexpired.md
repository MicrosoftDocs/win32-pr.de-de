---
title: ms-DS-User-Password-Expired-Attribut
description: Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abgelaufen ist.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-User-Password-Expired-Attributs
- AD-Schema des msDS-UserPasswordExpired-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a187f9d0b2be2feeca076d7c7eef82a34ca5827a9d07c76b2d711a5196f84ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425356"
---
# <a name="ms-ds-user-password-expired-attribute"></a>ms-DS-User-Password-Expired-Attribut

Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abgelaufen ist. TRUE, wenn das Kennwort abgelaufen ist; andernfalls False.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-Expired          |
| Ldap-Anzeigename | msDS-UserPasswordExpired             |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-Id-Guid    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
| Syntax            | [**Boolean**](s-boolean.md)         |



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
| System-Flags           | 0x00000014                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM ersetzt dieses Attribut das [**ADS \_ UF \_ PASSWORD \_ EXPIRED-Flag**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) des [**userAccountControl-Attributs.**](a-useraccountcontrol.md)

 

