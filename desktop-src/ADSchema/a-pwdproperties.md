---
title: Pwd-Properties-Attribut
description: Kenn Wort Eigenschaften. Teil der Domänen Richtlinie. Ein Bitfeld, das Komplexitäts-und Speicherbeschränkungen angibt.
ms.assetid: 9d73595f-508f-4562-a928-4833df977ab3
ms.tgt_platform: multiple
keywords:
- AD-Schema für Pwd-Properties-Attribut
- pwdproperties-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Pwd-Properties
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d8338e1bb8279aa5b80e5edaa536c6a246e4912
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957446"
---
# <a name="pwd-properties-attribute"></a>Pwd-Properties-Attribut

Kenn Wort Eigenschaften. Teil der Domänen Richtlinie. Ein Bitfeld, das Komplexitäts-und Speicherbeschränkungen angibt.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Pwd-Properties                                                                                                                                                                                                           |
| LDAP-Display-Name | pwdproperties                                                                                                                                                                                                            |
| Size              | Eine ganze Zahl. Domänen \_ Kennwort \_ Komplex 1, Domänen \_ Kennwort \_ Nein \_ \_ , Änderung 2, Domänen \_ Kennwort \_ nicht \_ Clear- \_ Änderung 4, Domänen \_ \_ Sperrungs Administratoren 8, Domänen \_ Kennwort- \_ Speicher \_ cleartext 16, Domänen Sperre \_ \_ Kennwort \_ ändern 32 |
| Berechtigung aktualisieren  | Domänen Administrator                                                                                                                                                                                                     |
| Aktualisierungshäufigkeit  | Wenn die Richtlinie für einen Benutzer geändert wird.                                                                                                                                                                                      |
| Attribute-Id      | 1.2.840.113556.1.4.93                                                                                                                                                                                                    |
| System-ID-GUID    | bf967a0b-0de6-11d0-a285-00aa003049e2                                                                                                                                                                                     |
| Syntax            | [**Enumeration**](s-enumeration.md)                                                                                                                                                                                     |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänen Richtlinie**](c-domainpolicy.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





