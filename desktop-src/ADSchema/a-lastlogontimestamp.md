---
title: Last-Logon-Timestamp-Attribut
description: Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- AD-Schema des Last-Logon-Timestamp-Attributs
- AD-Schema des lastLogonTimestamp-Attributs
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107240"
---
# <a name="last-logon-timestamp-attribute"></a>Last-Logon-Timestamp-Attribut

Dies ist der Zeitpunkt, zu dem sich der Benutzer zuletzt bei der Domäne angemeldet hat. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Jedes Mal, wenn sich ein Benutzer anmeldet, wird der Wert dieses Attributs vom DC gelesen. Wenn der Wert älter ist \[ `current_time - msDS-LogonTimeSyncInterval` \] , wird der Wert aktualisiert. Das erste Update nach der Erhöhung der Domänen Funktionsebene wird als 14 Tage minus zufälliger Prozentsatz von 5 Tagen berechnet.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| CN                | Zeitstempel der letzten Anmeldung                                                                                                   |
| LDAP-Display-Name | lastLogonTimestamp                                                                                                     |
| Size              | \-                                                                                                                     |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                                                                                       |
| Aktualisierungshäufigkeit  | Wenn sich der Benutzer anmeldet und dieser Wert älter als die aktuelle Zeit abzüglich des Werts von MSDS-logontimesyncinterval ist. |
| Attribute-Id      | 1.2.840.113556.1.4.1696                                                                                                |
| System-ID-GUID    | c0e20a04-0e5a-4ff3-9482-5efeaecd7060                                                                                   |
| Syntax            | [**Intervall**](s-interval.md)                                                                                         |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

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
| System-Only            | Richtig                                                              |
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
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
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
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | Richtig                              |
| Im globalen Katalog      | Richtig                              |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





