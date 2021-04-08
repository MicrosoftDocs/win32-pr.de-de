---
title: Trust-Attributes-Attribut
description: Dieses Attribut speichert die Vertrauens Attribute für eine vertrauenswürdige Domäne.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- AD-Schema für Trust-Attributes-Attribut
- trustatutributes-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744881"
---
# <a name="trust-attributes-attribute"></a>Trust-Attributes-Attribut

Dieses Attribut speichert die Vertrauens Attribute für eine vertrauenswürdige Domäne. Folgende Attributwerte sind möglich:

-   \_ \_ Nicht \_ transitives Vertrauens Attribut deaktivieren Transitivität.
-   \_ \_ \_ Die übergeordnete Vertrauensstellung der Trust-Attribut Struktur ist auf das übergeordnete Element der Organisationsstruktur
-   Vertrauensstellung des vertrauenswürdigen \_ Attribut \_ Baums \_ auf einen anderen Struktur Stamm in der Gesamtstruktur.
-   Vertrauens \_ Attribut \_ komplexer Darstellung \_ nur vertrauenswürdiger Link ist nur für den komplexer Darstellung-Client gültig.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Trust-Attributes                     |
| LDAP-Display-Name | trustatus Tributes                      |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.470               |
| System-ID-GUID    | 80a67e5a-9F 22-11D0-AFDD-00c04f-930c9 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | False                                                |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------|
| Link-ID                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | False                                                |
| Ist-einwertig       | Richtig                                                 |
| Ist indiziert             | False                                                |
| Im globalen Katalog      | Richtig                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| In verwendete Klassen        | [**Vertrauenswürdige Domäne**](c-trusteddomain.md)<br/> |



 

 





