---
title: Manager-Attribut
description: Enthält den Distinguished Name des Benutzers, der der Manager des Benutzers ist. Das Benutzerobjekt des Managers enthält eine DirectReports-Eigenschaft, die Verweise auf alle Benutzer Objekte enthält, deren Manager-Eigenschaften auf diesen Distinguished Name festgelegt sind.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- AD-Schema für Manager-Attribut
- AD-Schema für Manager-Attribut
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392288"
---
# <a name="manager-attribute"></a>Manager-Attribut

Enthält den Distinguished Name des Benutzers, der der Manager des Benutzers ist. Das Benutzerobjekt des Managers enthält eine DirectReports-Eigenschaft, die Verweise auf alle Benutzer Objekte enthält, deren Manager-Eigenschaften auf diesen Distinguished Name festgelegt sind.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| LDAP-Display-Name | manager                                                                     |
| Size              | \-                                                                          |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                      |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt und der Manager geändert werden muss. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID-GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | False                                                              |
| Ist-einwertig       | Richtig                                                               |
| Ist indiziert             | False                                                              |
| Im globalen Katalog      | Richtig                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | Richtig                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> |



 

 





