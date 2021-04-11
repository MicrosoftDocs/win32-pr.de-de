---
title: Trust-Partner-Attribut
description: Der Name der Domäne, mit der eine Vertrauensstellung vorhanden ist.
ms.assetid: 0b7c8e78-614b-46dd-8616-40d75b461639
ms.tgt_platform: multiple
keywords:
- AD-Schema für Trust-Partner-Attribut
- Trust Partner-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Trust-Partner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201a89e178515b270302b4d8541af64a63ad6813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107493"
---
# <a name="trust-partner-attribute"></a>Trust-Partner-Attribut

Der Name der Domäne, mit der eine Vertrauensstellung vorhanden ist.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Trust-Partner                               |
| LDAP-Display-Name | Trust Partner                                |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.            |
| Aktualisierungshäufigkeit  | Wenn eine neue Vertrauensstellung erstellt wird.                |
| Attribute-Id      | 1.2.840.113556.1.4.133                      |
| System-ID-GUID    | bf967a5d-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | Richtig                                                 |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | 1                                                    |
| Range-Upper            | 1024                                                 |
| Search-Flags           | 0x00000001                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





