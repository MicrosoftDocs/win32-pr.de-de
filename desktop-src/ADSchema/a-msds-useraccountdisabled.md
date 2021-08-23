---
title: ms-DS-User-Account-Disabled-Attribut
description: Gibt an, ob ein Konto aktiviert oder deaktiviert ist.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- MS-DS-User-Account-Disabled-Attribut AD-Schema
- MSDS-UserAccountDisabled-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f0744cd835fab641de4f4d3386304a342fe3902fcf1a67b3367dc15b7ee68f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544140"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>ms-DS-User-Account-Disabled-Attribut

Gibt an, ob ein Konto aktiviert oder deaktiviert ist. True, wenn das Konto deaktiviert ist; Andernfalls False.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Disabled          |
| Ldap-Anzeigename | msDS-UserAccountDisabled             |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID-GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
| Syntax            | [**Boolesch**](s-boolean.md)         |



## <a name="implementations"></a>Implementierungen

-   [**Adam**](#adam)

## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist einwertig       | True                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM ersetzt dieses Attribut das [**ADS \_ UF \_ ACCOUNTDISABLE-Flag**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) des [**userAccountControl-Attributs.**](a-useraccountcontrol.md)

 

