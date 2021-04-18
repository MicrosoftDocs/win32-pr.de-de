---
title: Lockout-Duration-Attribut
description: Die Zeitspanne, für die ein Konto aufgrund der Überschreitung des Lockout-Threshold gesperrt ist.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- AD-Schema für Lockout-Duration-Attribut
- AD-Schema für LockoutDuration-Attribut
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106338818"
---
# <a name="lockout-duration-attribute"></a>Lockout-Duration-Attribut

Die Zeitspanne, für die ein Konto gesperrt ist, weil der [**Sperr Schwellenwert**](a-lockoutthreshold.md) überschritten wurde. Dieser Wert wird als große ganze Zahl gespeichert, die den negativen Wert der Anzahl der 100-Nanosekunden-Intervalle ab dem Zeitpunkt darstellt, zu dem der Sperrungs [**Schwellen**](a-lockoutthreshold.md) Wert überschritten wird, der vergehen muss, bevor das Konto entsperrt wird.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| LDAP-Display-Name | LockoutDuration                      |
| Size              | \-                                   |
| Berechtigung aktualisieren  | Domänen Administrator                 |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-ID-GUID    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervall**](s-interval.md)       |



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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sperrungs Schwellenwert**](a-lockoutthreshold.md)
</dt> </dl>

 

 





