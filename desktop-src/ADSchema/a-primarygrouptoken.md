---
title: Primary-Group-Token-Attribut
description: Ein berechnetes Attribut, das zum Abrufen der Mitgliedschafts Liste einer Gruppe verwendet wird, z. b. Domänen Benutzer. Die komplette Mitgliedschaft dieser Gruppen wird aus Gründen der Skalierung nicht explizit gespeichert.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- AD-Schema des Primary-Group-Token-Attributs
- primarygrouptoken-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107607"
---
# <a name="primary-group-token-attribute"></a>Primary-Group-Token-Attribut

Ein berechnetes Attribut, das zum Abrufen der Mitgliedschafts Liste einer Gruppe verwendet wird, z. b. Domänen Benutzer. Die komplette Mitgliedschaft dieser Gruppen wird aus Gründen der Skalierung nicht explizit gespeichert.



| Eingabe | Wert |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-Token                        |
| LDAP-Display-Name | primarygrouptoken                          |
| Size              | 4 Bytes                                    |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.           |
| Aktualisierungshäufigkeit  | Jedes Mal, wenn sich eine primäre Gruppe von Objekten ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntax            | [**Enumeration**](s-enumeration.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist-einwertig       | Richtig                                |
| Ist indiziert             | False                               |
| Im globalen Katalog      | False                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



 

 





