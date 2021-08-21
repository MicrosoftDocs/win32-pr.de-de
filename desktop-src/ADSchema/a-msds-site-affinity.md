---
title: ms-DS-Site-Affinity-Attribut
description: Das Attribut ms-DS-Site-Affinity wird vom Sicherheitskonten-Manager für die Gruppenerweiterung während der Tokenauswertung verwendet.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- MS-DS-Site-Affinity-Attribut AD-Schema
- MSDS-Site-Affinity-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1d3fc359388f5303be808786a929840a409d29505949601b54bd9c7a8b18cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544580"
---
# <a name="ms-ds-site-affinity-attribute"></a>ms-DS-Site-Affinity-Attribut

Das **Attribut ms-DS-Site-Affinity** wird vom Sicherheitskonten-Manager für die Gruppenerweiterung während der Tokenauswertung verwendet.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| CN                | ms-DS-Site-Affinity                                                                     |
| Ldap-Anzeigename | msDS-Site-Affinity                                                                      |
| Size              | Blob mit mehreren Werten, wobei jeder Wert sizeof(GUID) + sizeof(LARGE \_ INTEGER) ist. |
| Aktualisieren von Berechtigungen  | \-                                                                                      |
| Updatehäufigkeit  | Standardmäßig alle drei Monate.                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.1443                                                                 |
| System-ID-GUID    | c17c5602-bcb7-46f0-9656-6370ca884b72                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                   |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | False                             |
| Ist indiziert             | True                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | False                             |
| Ist indiziert             | True                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | False                             |
| Ist indiziert             | True                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | False                             |
| Ist indiziert             | True                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | False                             |
| Ist indiziert             | True                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





