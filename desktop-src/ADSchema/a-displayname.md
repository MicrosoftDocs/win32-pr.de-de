---
title: Display-Name-Attribut
description: Der Anzeigename für ein Objekt.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Display-Name AD-Schema
- ad-Schema des displayName-Attributs
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d4be2c6823fa068f07a14ab478a797c0db92e4f91b25656439319da5a25db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049590"
---
# <a name="display-name-attribute"></a>Display-Name-Attribut

Der Anzeigename für ein Objekt. Dies ist in der Regel die Kombination aus Vorname, Anfangsname und Nachname des Benutzer.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------|
| CN                | Anzeigename                                                                 |
| Ldap-Anzeigename | displayName                                                                  |
| Size              | \-                                                                           |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                       |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und der Anzeigename geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-Id-Guid    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falsch                           |
| Is-Single-Valued       | Richtig                            |
| Ist indiziert             | Richtig                            |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
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
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Service-Class**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Adressbuchcontainer**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                |
| Ist einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| In verwendete Klassen        | [**Adressbuchcontainer**](c-addressbookcontainer.md)<br/> [**Adressvorlage**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Dienstklasse**](c-serviceclass.md)<br/> [**Dienstinstanz**](c-serviceinstance.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





