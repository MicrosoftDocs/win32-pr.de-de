---
title: Display-Name-Attribut
description: Der Anzeige Name für ein Objekt.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- AD-Schema für Display-Name-Attribut
- Display Name-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744257"
---
# <a name="display-name-attribute"></a>Display-Name-Attribut

Der Anzeige Name für ein Objekt. Dabei handelt es sich normalerweise um die Kombination aus dem Vornamen, dem mittleren Anfangs-und dem Nachnamen des Benutzers.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------|
| CN                | Anzeigename                                                                 |
| LDAP-Display-Name | displayName                                                                  |
| Size              | \-                                                                           |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                       |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt und der Anzeige Name geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-ID-GUID    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | Richtig                            |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Address-Template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Zertifikat-Vorlage**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienst Instanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





