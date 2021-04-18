---
title: ms-DS-allowed-to-Delegat-Attribut
description: Hierbei handelt es sich um ein Attribut für Dienst Konto Objekte (Computer-oder Benutzerkonten).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- AD-Schema für das "ms-DS-allowed-to-Delegat"-Attribut
- AD-Schema für das msDS-Zustellungs Attribut
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344134"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a>ms-DS-allowed-to-Delegat-Attribut

Hierbei handelt es sich um ein Attribut für Dienst Konto Objekte (Computer-oder Benutzerkonten). Sie enthält eine Liste von Dienst Prinzipal Namen (SPNs). Dieses Attribut wird verwendet, um einen Dienst so zu konfigurieren, dass er Dienst Tickets abrufen kann, die für die eingeschränkte Delegierung verwendet werden können.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-DS-allowed-to-Delegat-an                |
| LDAP-Display-Name | MSDS-Zuweisung                    |
| Size              | 0 bis 64K                                    |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | Selten                                |
| Attribute-Id      | 1.2.840.113556.1.4.1787                     |
| System-ID-GUID    | 800d94d7-b7a1-42A1-b14d-7cae1423d07f        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | False                                                              |
| Ist-einwertig       | False                                                              |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
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
| System-Only            | False                                                              |
| Ist-einwertig       | False                                                              |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
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
| System-Only            | False                                                              |
| Ist-einwertig       | False                                                              |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
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
| System-Only            | False                                                              |
| Ist-einwertig       | False                                                              |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
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
| System-Only            | False                                                              |
| Ist-einwertig       | False                                                              |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | False                                                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





