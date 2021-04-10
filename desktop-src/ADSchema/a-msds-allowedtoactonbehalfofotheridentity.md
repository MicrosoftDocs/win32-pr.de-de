---
title: ms-DS-allowed-to-act-on-Auftrag-of-Identity-Attribut
description: Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung verfügt, im Namen anderer Identitäten für Dienste, die als dieses Konto ausgeführt werden, zu agieren.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- AD-Schema "ms-DS-allowed-to-act-on-Do-of-Identity-Attribute"
- AD-Schema für das msDS-Zustellungs Attribut
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dacd532b1d8a55b3656dc1d65fc1ebd940476c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859861"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a>ms-DS-allowed-to-act-on-Auftrag-of-Identity-Attribut

Dieses Attribut wird für Zugriffs Überprüfungen verwendet, um zu bestimmen, ob ein Anforderer über die Berechtigung verfügt, im Namen anderer Identitäten für Dienste, die als dieses Konto ausgeführt werden, zu agieren.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------|
| CN                | ms-DS-allowed-to-act-on-Do-of-other-Identity    |
| LDAP-Display-Name | MSDS-Zuweisung von "msDS--ID"            |
| Size              | \-                                                  |
| Berechtigung aktualisieren  | \-                                                  |
| Aktualisierungshäufigkeit  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.4.2182                             |
| System-ID-GUID    | 3b78c3e5-b-46bd-a0b8-9d18116ddc79                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Richtig                                                               |
| Ist-einwertig       | Richtig                                                               |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
| Range-Lower            | 0                                                                  |
| Range-Upper            | 132096                                                             |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





