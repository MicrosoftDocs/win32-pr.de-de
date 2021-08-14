---
title: MS-DS-Per-User-Trust-Quota-Attribut
description: Wird verwendet, um ein benutzerspezifisches Kontingent zum Erstellen von Trusted-Domain zu erzwingen, die durch das neue Steuerelementzugriffsrecht Create-Inbound-Forest-Trust autorisiert sind.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-DS-Per-User-Trust-Quota-Attributs
- AD-Schema des msDS-PerUserTrustQuota-Attributs
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fc51a6e3e3e9f3d14534487590985197ed7c97fbca8bc1042108bfcdba97530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425826"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a>MS-DS-Per-User-Trust-Quota-Attribut

Wird verwendet, um ein benutzerspezifisches Kontingent zum Erstellen von Trusted-Domain zu erzwingen, die durch das neue Steuerelementzugriffsrecht Create-Inbound-Forest-Trust autorisiert sind. Dieses Attribut schränkt die Anzahl Trusted-Domain-Objekten ein, die von einem einzelnen Benutzer ohne Administratorrechte erstellt werden können.



| Eingabe | Wert |
|-------------------|-------------------------------------------|
| CN                | MS-DS-per-User-Trust-Quota                |
| Ldap-Anzeigename | msDS-PerUserTrustQuota                    |
| Size              | \-                                        |
| Aktualisieren von Berechtigungen  | Domänenadministrator                      |
| Updatehäufigkeit  | Bei der Gesamtstrukturerstellung und selten danach. |
| Attribute-Id      | 1.2.840.113556.1.4.1788                   |
| System-Id-Guid    | d161adf0-ca24-4993-a3aa-8b2c981302e8      |
| Syntax            | [**Enumeration**](s-enumeration.md)      |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Is-Single-Valued       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





