---
title: Max-Pwd-Age-Attribut
description: Die maximale Zeitspanne in Intervallen von 100 Nanosekunden ist ein Kennwort gültig.
ms.assetid: b4b48207-6481-42a1-b848-6baf37a367ce
ms.tgt_platform: multiple
keywords:
- AD-Schema des Max-Pwd-Age-Attributs
- MAXPwdAge-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Max-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93c647d05d0ddca2947878b908d3a7f7f5b293e308c6e799fb6e1d85db7e97ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301040"
---
# <a name="max-pwd-age-attribute"></a>Max-Pwd-Age-Attribut

Die maximale Zeitspanne in Intervallen von 100 Nanosekunden ist ein Kennwort gültig. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen ab dem Zeitpunkt darstellt, zu dem das Kennwort festgelegt wurde, bevor das Kennwort abläuft.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Max-Pwd-Age                          |
| Ldap-Anzeigename | maxPwdAge                            |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | Domänenadministrator                 |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.74                |
| System-ID-GUID    | bf9679bb-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Ist einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Ist einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Ist einwertig       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Is-Single-Valued       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Is-Single-Valued       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falsch                                                                                                                                                 |
| Is-Single-Valued       | Richtig                                                                                                                                                  |
| Ist indiziert             | Falsch                                                                                                                                                 |
| Im globalen Katalog      | Falsch                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





