---
title: Title-Attribut
description: Enthält die Position des Benutzers. Diese Eigenschaft wird normalerweise verwendet, um die formale Berufsbezeichnung anzugeben, wie z. b. Senior Programmer, anstelle einer berufsklasse, z. b. Programmierer. Sie wird in der Regel nicht für Suffix-Titel wie Esq verwendet. oder DDS.
ms.assetid: 4a6899a7-ddbf-4dd0-b088-3739716f33df
ms.tgt_platform: multiple
keywords:
- AD-Schema für Titel Attribut
- AD-Schema für Titel Attribut
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbb4dae862db9fc363b22647bd5e56a98e9e60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859748"
---
# <a name="title-attribute-ad-schema"></a>Title-Attribut (AD-Schema)

Enthält die Position des Benutzers. Diese Eigenschaft wird normalerweise verwendet, um die formale Berufsbezeichnung anzugeben, wie z. b. Senior Programmer, anstelle einer berufsklasse, z. b. Programmierer. Sie wird in der Regel nicht für Suffix-Titel wie Esq verwendet. oder DDS.



| Eingabe | Wert |
|-------------------|---------------------------------------------------------------------------|
| CN                | Titel                                                                     |
| LDAP-Display-Name | title                                                                     |
| Size              | \-                                                                        |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                    |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt wird, und wenn der Titel geändert werden muss. |
| Attribute-Id      | 2.5.4.12                                                                  |
| System-ID-GUID    | bf967a55-0de6-11d0-a285-00aa003049e2                                      |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                               |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 64                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                              |
| MAPI-Id                | 0x3a17                                                                                                                          |
| System-Only            | False                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                            |
| Ist indiziert             | False                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                    |
| Range-Lower            | 1                                                                                                                               |
| Range-Upper            | 128                                                                                                                             |
| Search-Flags           | 0x00000000                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                      |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



 

 





