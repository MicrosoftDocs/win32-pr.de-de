---
title: MS-DS-Machine-Account-Quota-Attribut
description: Die Anzahl der Computerkonten, die ein Benutzer in einer Domäne erstellen darf.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- AD-Schema des MS-DS-Machine-Account-Quota-Attributs
- MS-DS-MachineAccountQuota-Attribut AD-Schema
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56790f601e9784ddeb55c47450cab9b1f3bce468d8d15c7c44e0e57344525839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961169"
---
# <a name="ms-ds-machine-account-quota-attribute"></a>MS-DS-Machine-Account-Quota-Attribut

Die Anzahl der Computerkonten, die ein Benutzer in einer Domäne erstellen darf.



| Eingabe | Wert |
|-------------------|--------------------------------------------------|
| CN                | MS-DS-Machine-Account-Quota                      |
| Ldap-Anzeigename | ms-DS-MachineAccountQuota                        |
| Size              | 4 Bytes                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator                             |
| Updatehäufigkeit  | Immer dann, wenn das Kontingent für eine Domäne geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.1411                          |
| System-ID-GUID    | d064fb68-1480-11d3-91c1-0000f87a57d4             |
| Syntax            | [**Enumeration**](s-enumeration.md)             |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist einwertig       | True                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist einwertig       | True                                         |
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
| Ist einwertig       | True                                         |
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



 

 





