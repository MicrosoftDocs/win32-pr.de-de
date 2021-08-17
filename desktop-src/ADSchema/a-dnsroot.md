---
title: Dns-Root-Attribut
description: Der oberste DNS-Domänenname, der einer Domänen-/Verzeichnispartition zugewiesen ist.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Dns-Root AD-Schema
- AD-Schema des dnsRoot-Attributs
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f87acecb86fcd8ca8af4bbc2917dbe5381deaf4e5722a5803d31f186e57e04d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961579"
---
# <a name="dns-root-attribute"></a>Dns-Root-Attribut

Der oberste DNS-Domänenname, der einer Domänen-/Verzeichnispartition zugewiesen ist. Dies wird für ein crossRef-Objekt festgelegt und unter anderem für die Generierung von Empfehlungen verwendet. Beim Durchsuchen einer gesamten Domänenstruktur muss die Suche am Dns-Root werden. Dieses Attribut kann mehrere Werte haben. In diesem Fall werden mehrere Empfehlungen generiert.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| Ldap-Anzeigename | dnsRoot                                     |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.            |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-Id-Guid    | bf967959-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Is-Single-Valued       | False                                      |
| Ist indiziert             | True                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Ref-übergreifend**](c-crossref.md)<br/> |



 

 





