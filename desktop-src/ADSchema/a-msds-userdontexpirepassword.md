---
title: ms-DS-User-dont-expire-Password-Attribut
description: Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abläuft.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-User-dont-expire-Password-Attribut
- AD-Schema des msDS-userdontexpirepassword-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107768"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>ms-DS-User-dont-expire-Password-Attribut

Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abläuft. True, wenn das Kennwort nicht abläuft. andernfalls false.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-nicht-ablaufen-Kennwort      |
| LDAP-Display-Name | MSDS-userdontexpirepassword          |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID-GUID    | 8788193a-2925-43d9-A221-bb7fff397675 |
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
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Objekt**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Bemerkungen

In Adam ersetzt dieses Attribut das ADS-Flag "nicht [**\_ \_ \_ ablaufen \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " des Attributs " [**userAccountControl**](a-useraccountcontrol.md) ".

 

