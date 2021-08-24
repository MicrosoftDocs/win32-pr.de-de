---
title: ms-DS-Allowed-To-Delegate-To-Attribut
description: Dies ist ein Attribut für Dienstkontoobjekte (Computer oder Benutzerkonto).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- MS-DS-Allowed-To-Delegate-To-Attribut AD-Schema
- AD-Schema des msDS-AllowedToDelegateTo-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3a91abc375e67806387170ee6bda450c6f2bf167a3971f9808cd04e4c24d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704930"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>ms-DS-Allowed-To-Delegate-To-Attribut

Dies ist ein Attribut für Dienstkontoobjekte (Computer oder Benutzerkonto). Sie enthält eine Liste der Dienstprinzipalnamen (Service Principal Names, SPNs). Dieses Attribut wird verwendet, um einen Dienst so zu konfigurieren, dass er Diensttickets abrufen kann, die für die eingeschränkte Delegierung verwendet werden können.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Allowed-to-Delegate-To                |
| Ldap-Anzeigename | msDS-AllowedToDelegateTo                    |
| Size              | 0 bis 64 KB                                    |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | Selten                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-ID-GUID    | 800d94d7-b7a1-42a1-b14d-7cae1423d07f        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falsch                                                              |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falsch                                                              |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falsch                                                              |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falsch                                                              |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Falsch                                                              |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





