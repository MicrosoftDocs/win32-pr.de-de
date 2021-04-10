---
title: ms-DS-User-Password-abgelaufenes Attribut
description: Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abgelaufen ist.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-User-Password-abgelaufenes Attribut
- adschema des msDS-userpasswordexpired-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104213787"
---
# <a name="ms-ds-user-password-expired-attribute"></a>ms-DS-User-Password-abgelaufenes Attribut

Gibt an, ob das Kennwort für das Konto, auf das dieses Attribut verweist, abgelaufen ist. True, wenn das Kennwort abgelaufen ist. andernfalls false.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-abgelaufen          |
| LDAP-Display-Name | MSDS-userpasswordexpired             |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID-GUID    | 565c7ab5-e13e-47l6-ABB5-de741806f 125 |
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

In Adam ersetzt dieses Attribut das Flag " [**ADS- \_ \_ Kennwort \_ abgelaufen**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " des Attributs " [**userAccountControl**](a-useraccountcontrol.md) ".

 

