---
title: UNC-Name-Attribut
description: Der Name der universellen Benennungs Konvention für freigegebene Volumes und Drucker.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- AD-Schema für UNC-Name-Attribut
- uncname-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e06bc54ebb035a491e2d93a1c372e2d46fc43f76
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346152"
---
# <a name="unc-name-attribute"></a>UNC-Name-Attribut

Der Name der universellen Benennungs Konvention für freigegebene Volumes und Drucker.



| Eingabe | Wert |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| LDAP-Display-Name | uNCName                                       |
| Size              | \-                                            |
| Berechtigung aktualisieren  | Domänen Administrator                          |
| Aktualisierungshäufigkeit  | Wenn neue Volumes oder Druck Warteschlangen erstellt werden. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-ID-GUID    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | False                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| In verwendete Klassen        | [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | False                                                                                                                                                                                     |
| Ist-einwertig       | Richtig                                                                                                                                                                                      |
| Ist indiziert             | Richtig                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| In verwendete Klassen        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-connectionpolicy**](c-msprint-connectionpolicy.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-connectionpolicy**](c-msprint-connectionpolicy.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-connectionpolicy**](c-msprint-connectionpolicy.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-connectionpolicy**](c-msprint-connectionpolicy.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Lautstärke**](c-volume.md)<br/> |



 

 





