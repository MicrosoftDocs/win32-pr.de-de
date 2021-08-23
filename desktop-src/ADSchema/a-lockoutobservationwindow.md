---
title: Lock-Out-Observation-Window-Attribut
description: Der Zeitbereich in Intervallen von 100 Nanosekunden, in dem das System die falsche Anmeldeanzahl erhöht.
ms.assetid: a1929c32-cd05-43ca-9d4a-554683991696
ms.tgt_platform: multiple
keywords:
- AD-Schema des Lock-Out-Observation-Window-Attributs
- lockOutObservationWindow-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Lock-Out-Observation-Window
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0850c966b9a6a200779b2c567cecbfd4c68f38af1f45c6196a2f913c9e9e13fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705760"
---
# <a name="lock-out-observation-window-attribute"></a>Lock-Out-Observation-Window-Attribut

Der Zeitbereich in Intervallen von 100 Nanosekunden, in dem das System die falsche Anmeldeanzahl erhöht.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Fenster "Überwachung der Sperre aus"          |
| Ldap-Anzeigename | lockOutObservationWindow             |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | Domänenadministrator                 |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.61                |
| System-Id-Guid    | bf9679a4-0de6-11d0-a285-00aa003049e2 |
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
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
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
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
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
| System-Only            | False                                                                                                                                                 |
| Is-Single-Valued       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
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
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
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
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
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
| System-Only            | False                                                                                                                                                 |
| Ist einwertig       | True                                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| In verwendete Klassen        | [**Domänenrichtlinie**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





