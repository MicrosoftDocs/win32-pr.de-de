---
title: Lockout-Time-Attribut
description: Das Datum und die Uhrzeit (UTC), an denen dieses Konto gesperrt wurde.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Lockout-Time-Attribut
- AD-Schema des lockoutTime-Attributs
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adebe8bf76ba04fe4ba774726da7cd5c54e64ab1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342913"
---
# <a name="lockout-time-attribute"></a>Lockout-Time-Attribut

Das Datum und die Uhrzeit (UTC), an denen dieses Konto gesperrt wurde. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Der Wert 0 (null) bedeutet, dass das Konto zurzeit nicht gesperrt ist.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Lockout-Time                                                                     |
| LDAP-Display-Name | lockoutTime                                                                      |
| Size              | 8 Bytes                                                                          |
| Berechtigung aktualisieren  | Domänen Administrator                                                             |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt wird und die Sperr Zeit geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.662                                                           |
| System-ID-GUID    | 28630ebf -41d5-11d1-a9c1-0000 C1                                             |
| Syntax            | [**Intervall**](s-interval.md)                                                   |



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
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Objekt**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur.

Dieser Attribut Wert wird nur zurückgesetzt, wenn das Konto erfolgreich bei angemeldet ist. Dies bedeutet, dass dieser Wert möglicherweise nicht NULL ist, aber das Konto nicht gesperrt ist. Um genau festzustellen, ob das Konto gesperrt ist, müssen Sie dieser Zeit die [**Lockout-Dauer**](a-lockoutduration.md) hinzufügen und das Ergebnis mit der aktuellen Zeit vergleichen, wobei lokale Zeitzonen und Sommerzeit berücksichtigt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**Sperr Dauer**](a-lockoutduration.md)
</dt> </dl>

 

