---
title: User-Principal-Name-Attribut
description: Dieses Attribut enthält den UPN, bei dem es sich um einen Anmeldenamen im Internetformat für einen Benutzer handelt, der auf dem Internetstandard RFC 822 basiert.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- AD-Schema des Benutzerprinzipalnamenattributs
- userPrincipalName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba8ac5196de660c4cff4b90801470581cc660491902ec5b48f0ced8337c498b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835285"
---
# <a name="user-principal-name-attribute"></a>User-Principal-Name-Attribut

Dieses Attribut enthält den UPN, bei dem es sich um einen Anmeldenamen im Internetformat für einen Benutzer handelt, der auf dem Internetstandard [RFC 822 basiert.](https://www.ietf.org/rfc/rfc0822.txt) Der UPN ist kürzer als der Distinguished Name und leichter zu merken. Nach Der Konvention sollte dies dem E-Mail-Namen des Benutzers zuordnen. Der für dieses Attribut festgelegte Wert entspricht der Länge der Benutzer-ID und des Domänennamens. Weitere Informationen zu diesem Attribut finden Sie unter [Benutzerbenennungsattribute.](/windows/desktop/AD/naming-properties)



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Benutzerprinzipalname                         |
| Ldap-Anzeigename | userPrincipalName                           |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.      |
| Updatehäufigkeit  | Theoretisch sollte sich dies nie ändern.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-Id-Guid    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch        |
| Is-Single-Valued       | Richtig         |
| Ist indiziert             | Richtig         |
| Im globalen Katalog      | Richtig         |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| System-Only            | Falsch                             |
| Is-Single-Valued       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Hinweise

In ADAM muss dieses Attribut nicht im Rfc 822-Format des Internetstandards vorliegen. kann ein einfacher Name sein.

 

