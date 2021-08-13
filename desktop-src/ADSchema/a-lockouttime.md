---
title: Lockout-Time-Attribut
description: Das Datum und die Uhrzeit (UTC), zu der dieses Konto gesperrt wurde.
ms.assetid: 4a0a66a3-9f7f-48ec-9b96-a9c3e72b2b6b
ms.tgt_platform: multiple
keywords:
- Lockout-Time AD-Attributschema
- lockoutTime-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Lockout-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 900f605ce6fed989526440dc1c4add9fdff59ca04ca1534ac5d026feb1a3b86a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301610"
---
# <a name="lockout-time-attribute"></a>Lockout-Time-Attribut

Das Datum und die Uhrzeit (UTC), zu der dieses Konto gesperrt wurde. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Der Wert 0 bedeutet, dass das Konto derzeit nicht gesperrt ist.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Lockout-Time                                                                     |
| Ldap-Anzeigename | lockoutTime                                                                      |
| Size              | 8 Bytes                                                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                                             |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und wann immer sich die Sperrzeit ändern muss. |
| Attribute-Id      | 1.2.840.113556.1.4.662                                                           |
| System-ID-GUID    | 28630ebf-41d5-11d1-a9c1-0000f80367c1                                             |
| Syntax            | [**Intervall**](s-interval.md)                                                   |



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
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="remarks"></a>Hinweise

Der hohe Teil dieser großen ganzen Zahl entspricht dem **dwHighDateTime-Member** der [**FILETIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) und der untere Teil dem **dwLowDateTime-Member** der **FILETIME-Struktur.**

Dieser Attributwert wird nur zurückgesetzt, wenn das Konto erfolgreich angemeldet wurde. Dies bedeutet, dass dieser Wert möglicherweise ungleich 0 (null) ist, das Konto jedoch nicht gesperrt ist. Um genau zu bestimmen, ob das Konto gesperrt ist, müssen Sie die [**Sperrdauer**](a-lockoutduration.md) zu diesem Zeitpunkt hinzufügen und das Ergebnis mit der aktuellen Zeit vergleichen, wobei lokale Zeitzonen und Sommerzeit berücksichtigt werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**Sperrdauer**](a-lockoutduration.md)
</dt> </dl>

 

