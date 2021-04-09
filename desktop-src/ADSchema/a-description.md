---
title: Description-Attribut (AD-Schema)
description: Enthält die Beschreibung, die für ein-Objekt angezeigt werden soll. Dieser Wert wird für die Abwärtskompatibilität in einigen Fällen als einwertig eingeschränkt, kann aber in anderen mehr wertig sein. Siehe Hinweise.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Description-Attribut AD-Schema
- Description-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ccb155c9c65a42c29a022a6912b7aea7087477
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744273"
---
# <a name="description-attribute-ad-schema"></a>Description-Attribut (AD-Schema)

Enthält die Beschreibung, die für ein-Objekt angezeigt werden soll. Dieser Wert wird für die Abwärtskompatibilität in einigen Fällen als einwertig eingeschränkt, kann aber in anderen mehr wertig sein. Siehe Hinweise.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | BESCHREIBUNG                                 |
| LDAP-Display-Name | description                                 |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.      |
| Aktualisierungshäufigkeit  | Immer, wenn die Beschreibung geändert werden muss.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-ID-GUID    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| Link-ID                | \-                                                                           |
| MAPI-Id                | 0x806f                                                                       |
| System-Only            | False                                                                        |
| Ist-einwertig       | False                                                                        |
| Ist indiziert             | False                                                                        |
| Im globalen Katalog      | Richtig                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                         |
| MAPI-Id                | 0x806f                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Ist-einwertig       | False                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| In verwendete Klassen        | [**groupof uniquumames**](c-groupofuniquenames.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x806f                          |
| System-Only            | False                           |
| Ist-einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806f                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupof uniquumames**](c-groupofuniquenames.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**ipservice**](c-ipservice.md)<br/> [**ipprotocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ist**](c-ipnetwork.md)<br/> [**Netzwerkgruppe**](c-nisnetgroup.md)<br/> [**Bild Map**](c-nismap.md)<br/> [**nisobject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806f                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupof uniquumames**](c-groupofuniquenames.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**ipservice**](c-ipservice.md)<br/> [**ipprotocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ist**](c-ipnetwork.md)<br/> [**Netzwerkgruppe**](c-nisnetgroup.md)<br/> [**Bild Map**](c-nismap.md)<br/> [**nisobject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806f                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupof uniquumames**](c-groupofuniquenames.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**ipservice**](c-ipservice.md)<br/> [**ipprotocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ist**](c-ipnetwork.md)<br/> [**Netzwerkgruppe**](c-nisnetgroup.md)<br/> [**Bild Map**](c-nismap.md)<br/> [**nisobject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806f                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| In verwendete Klassen        | [**groupof uniquumames**](c-groupofuniquenames.md)<br/> [**Sam-Domäne**](c-samdomain.md)<br/> [**Nach oben**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixgroup**](c-posixgroup.md)<br/> [**ipservice**](c-ipservice.md)<br/> [**ipprotocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ist**](c-ipnetwork.md)<br/> [**Netzwerkgruppe**](c-nisnetgroup.md)<br/> [**Bild Map**](c-nismap.md)<br/> [**nisobject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Das Description-Attribut wird als mehr wertiges Attribut im Schema für die Fälle implementiert, in denen dies zulässig ist. Bei einem Objekt, das keine Sam-verwaltete Klasse ist, ist die Beschreibung mehr wertig. Bei einem Attribut, bei dem es sich um eine von Sam verwaltete Klasse handelt, ist das Beschreibungs Attribut einwertig. Sam Managed Classes ist für Dinge wie z. b. Sicherheits Prinzipale. Wenn Sie z. b. einen Container oder eine eigene Klasse haben, können Sie mit dem Schema mehrere Werte verwenden. Dieses Verhalten des Description-Attributs ist aus Gründen der Abwärtskompatibilität mit früheren Betriebssystemen, da das Attribut in den SAM-APIs vorhanden war, bevor AD vorhanden war.

 

 





