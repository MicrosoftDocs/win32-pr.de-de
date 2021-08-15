---
title: Description-Attribut (AD-Schema)
description: Enthält die Beschreibung, die für ein -Objekt angezeigt werden soll. Dieser Wert ist aus Gründen der Abwärtskompatibilität in einigen Fällen als einwertige Werte eingeschränkt, in anderen kann er jedoch mehrwertige Werte haben. Siehe Hinweise.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Beschreibungsattribut AD-Schema
- Beschreibungsattribut AD-Schema
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f53c344b026a89a3f579d1eb7fc7002a8a0410d28fd9b43d05882a4285eb73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961728"
---
# <a name="description-attribute-ad-schema"></a>Description-Attribut (AD-Schema)

Enthält die Beschreibung, die für ein -Objekt angezeigt werden soll. Dieser Wert ist aus Gründen der Abwärtskompatibilität in einigen Fällen als einwertige Werte eingeschränkt, in anderen kann er jedoch mehrwertige Werte haben. Siehe Hinweise.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | BESCHREIBUNG                                 |
| Ldap-Anzeigename | description                                 |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.      |
| Updatehäufigkeit  | Jedes Mal, wenn sich die Beschreibung ändern muss.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-Id-Guid    | bf967950-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|------------------------------------------------------------------------------|
| Link-ID                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | False                                                                        |
| Is-Single-Valued       | False                                                                        |
| Ist indiziert             | False                                                                        |
| Im globalen Katalog      | True                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Is-Single-Valued       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | True                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | False                           |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Is-Single-Valued       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**Nismap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Is-Single-Valued       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**Nismap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**Nismap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**Nismap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Hinweise

Das description-Attribut wird als mehrwertiges Attribut im Schema für die Fälle implementiert, in denen dies zulässig ist. Für ein Objekt, das keine verwaltete SAM-Klasse ist, ist die Beschreibung mehrwertiger Art. Bei einem Attribut, das eine verwaltete SAM-Klasse ist, ist das Description-Attribut einwertig. Verwaltete SAM-Klassen sind für Dinge wie Sicherheitsprinzipale vorgesehen. Wenn Sie z. B. über einen Container oder eine eigene Klasse verfügen, können Sie im Schema mehrere Werte verwenden. Dieses Verhalten des Description-Attributs dient der Abwärtskompatibilität mit früheren Betriebssystemen, da das Attribut in den SAM-APIs vorhanden war, bevor AD vorhanden war.

 

 





