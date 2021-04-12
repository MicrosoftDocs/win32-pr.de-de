---
title: ms-DS-User-Account-deaktiviertes Attribut
description: Gibt an, ob ein Konto aktiviert oder deaktiviert ist.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- AD-Schema "ms-DS-User-Account-deaktiviertes Attribut"
- AD-Schema für das msDS-useraccountdeaktiviertes Attribut
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a01c0b83599a8d6309f6639b94f5d0321180df
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480343"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>ms-DS-User-Account-deaktiviertes Attribut

Gibt an, ob ein Konto aktiviert oder deaktiviert ist. True, wenn das Konto deaktiviert ist. andernfalls false.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Benutzer-Konto-deaktiviert          |
| LDAP-Display-Name | MSDS-useraccountdeaktiviert             |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID-GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

In Adam ersetzt dieses Attribut das [**ADS- \_ \_ accountdeaktiviert**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) -Flag des [**userAccountControl**](a-useraccountcontrol.md) -Attributs.

 

