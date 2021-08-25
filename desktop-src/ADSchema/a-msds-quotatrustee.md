---
title: ms-DS-Quota-Trustee-Attribut
description: Die SID des Sicherheitsprinzipals, für den das Kontingent zugewiesen wird.
ms.assetid: 4da8f731-0a8f-4d8a-a4e7-81ed881a30b5
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-Quota-Trustee-Attributs
- AD-Schema des msDS-QuotaTrustee-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Quota-Trustee
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b453a3f48da5af7564fdb79f81d22a15a5b72450a68f22112c59ebfb2a749ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803620"
---
# <a name="ms-ds-quota-trustee-attribute"></a>ms-DS-Quota-Trustee-Attribut

Die SID des Sicherheitsprinzipals, für den das Kontingent zugewiesen wird.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-Quota-Trustee                  |
| Ldap-Anzeigename | msDS-QuotaTrustee                    |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1844              |
| System-Id-Guid    | 16378906-4ea5-49be-a8d1-bfd41dff4f65 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Is-Single-Valued       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Is-Single-Valued       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Is-Single-Valued       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------|
| Link-ID                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | False                                                         |
| Ist einwertig       | True                                                          |
| Ist indiziert             | False                                                         |
| Im globalen Katalog      | False                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                  |
| Range-Lower            | 0                                                             |
| Range-Upper            | 28                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| In verwendete Klassen        | [**ms-DS-Quota-Control**](c-msds-quotacontrol.md)<br/> |



 

 





