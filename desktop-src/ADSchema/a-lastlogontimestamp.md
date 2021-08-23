---
title: Last-Logon-Timestamp-Attribut
description: Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs "Last-Logon-Timestamp"
- lastLogonTimestamp-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaea56a7456a46b7583633992f77e6fd836276151e6c9f6b792ba1abdd36b4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322150"
---
# <a name="last-logon-timestamp-attribute"></a>Last-Logon-Timestamp-Attribut

Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Wenn sich ein Benutzer anmeldet, wird der Wert dieses Attributs vom DC gelesen. Wenn der Wert älter \[ `current_time - msDS-LogonTimeSyncInterval` \] ist, wird der Wert aktualisiert. Das erste Update nach der Erhöhung der Domänenfunktionsebene wird als 14 Tage abzüglich des zufälligen Prozentsatzes von 5 Tagen berechnet.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| CN                | Letzter Anmeldezeitstempel                                                                                                   |
| Ldap-Anzeigename | lastLogonTimestamp                                                                                                     |
| Size              | \-                                                                                                                     |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                                                                                       |
| Updatehäufigkeit  | Wenn sich der Benutzer anmeldet und dieser Wert älter als die aktuelle Uhrzeit ist, abzüglich des Werts von msDS-LogonTimeSyncInterval. |
| Attribute-Id      | 1.2.840.113556.1.4.1696                                                                                                |
| System-ID-GUID    | c0e20a04-0e5a-4ff3-9482-5efeaecd7060                                                                                   |
| Syntax            | [**Intervall**](s-interval.md)                                                                                         |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
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
| System-Only            | Richtig                                                              |
| Ist einwertig       | Richtig                                                              |
| Ist indiziert             | Falsch                                                             |
| Im globalen Katalog      | Falsch                                                             |
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
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Falsch                             |
| Im globalen Katalog      | Falsch                             |
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
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falsch                             |
| Ist einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





