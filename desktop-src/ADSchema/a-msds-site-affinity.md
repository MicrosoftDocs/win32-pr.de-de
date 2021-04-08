---
title: ms-DS-Site-Affinitäts Attribut
description: Das Attribut "ms-DS-Site-Affinität" wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.
ms.assetid: c05df70a-adbb-48e0-bdcd-c1d83a2e43bd
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Site-Affinitäts Attribut
- AD-Schema für MSDS-Site-Affinitäts Attribut
topic_type:
- apiref
api_name:
- ms-DS-Site-Affinity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dd3ed17b07c73d9e7a6a2d93d93463e1dea40fc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859834"
---
# <a name="ms-ds-site-affinity-attribute"></a>ms-DS-Site-Affinitäts Attribut

Das Attribut " **ms-DS-Site-Affinität** " wird vom Sicherheits Konten-Manager für die Gruppen Erweiterung während der tokenbewertung verwendet.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| CN                | ms-DS-Site-Affinität                                                                     |
| LDAP-Display-Name | MSDS-Site-Affinität                                                                      |
| Size              | Binary BLOB mit mehreren Werten, wobei jeder Wert sizeof (GUID) + sizeof (Large \_ Integer) ist. |
| Berechtigung aktualisieren  | \-                                                                                      |
| Aktualisierungshäufigkeit  | Standardmäßig alle drei Monate.                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.1443                                                                 |
| System-ID-GUID    | c17c5602-bcb7-46f0-9656-6370ca884b72                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                   |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | False                             |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| Ist-einwertig       | False                             |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| Ist-einwertig       | False                             |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| Ist-einwertig       | False                             |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| Ist-einwertig       | False                             |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





