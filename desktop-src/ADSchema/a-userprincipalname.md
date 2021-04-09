---
title: Benutzer Prinzipal Name-Attribut
description: Dieses Attribut enthält den UPN, bei dem es sich um einen Anmelde Namen im Internet Format für einen Benutzer handelt, der auf dem Internet Standard RFC 822 basiert.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Benutzer Prinzipal Namen-Attribut
- userPrincipalName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957432"
---
# <a name="user-principal-name-attribute"></a>Benutzer Prinzipal Name-Attribut

Dieses Attribut enthält den UPN, bei dem es sich um einen Anmelde Namen im Internet Format für einen Benutzer handelt, der auf dem Internet Standard [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)basiert. Der UPN ist kürzer als der Distinguished Name und ist leichter zu merken. Gemäß der Konvention sollte dies dem e-Mail-Namen des Benutzers entsprechen. Der für dieses Attribut festgelegte Wert ist gleich der Länge der Benutzer-ID und des Domänen Namens. Weitere Informationen zu diesem Attribut finden Sie unter [Benutzer Benennungs Attribute](/windows/desktop/AD/naming-properties).



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Benutzerprinzipalname                         |
| LDAP-Display-Name | userPrincipalName                           |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.      |
| Aktualisierungshäufigkeit  | Theoretisch sollte sich dies nie ändern.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-ID-GUID    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | False        |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | Richtig         |
| Im globalen Katalog      | Richtig         |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Bemerkungen

In Adam muss dieses Attribut nicht im Internet Standard RFC 822-Format vorliegen. Dies kann ein einfacher Name sein.

 

