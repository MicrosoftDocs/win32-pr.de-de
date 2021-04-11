---
title: ms-DS-User-Password-not-required-Attribut
description: Gibt an, ob für das Konto, auf das dieses Attribut verweist, ein Kennwort erforderlich ist.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-Password-not-required\"-Attribut AD-Schema"
- "\"ms-DS-userpasswordnotrequired\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123067"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>ms-DS-User-Password-not-required-Attribut

Gibt an, ob für das Konto, auf das dieses Attribut verweist, ein Kennwort erforderlich ist. True, wenn ein Kennwort nicht erforderlich ist. andernfalls false.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Password-nicht erforderlich     |
| LDAP-Display-Name | ms-DS-userpasswordnotrequired        |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID-GUID    | 8f 066172-a25e-4B53-8dcd-0a67d5b883d |
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

In Adam ersetzt dieses Attribut das ADS-Flag-Flag " [**\_ \_ \_ notreqd**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " des Attributs " [**userAccountControl**](a-useraccountcontrol.md) ".

 

