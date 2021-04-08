---
title: Keywords-Attribut
description: Eine Liste von Schlüsselwörtern, die verwendet werden können, um einen bestimmten Verbindungspunkt zu suchen.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Schlüsselwort Attribut AD-Schema
- Schlüsselwort Attribut AD-Schema
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5c1fba475505ee03cda4813f90a28d1c91fb69
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744809"
---
# <a name="keywords-attribute"></a>Keywords-Attribut

Eine Liste von Schlüsselwörtern, die verwendet werden können, um einen bestimmten Verbindungspunkt zu suchen.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Keywords                                    |
| LDAP-Display-Name | keywords                                    |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-ID-GUID    | bf967993-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|----------------------------------------------------------|
| Link-ID                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | False                                                    |
| Ist-einwertig       | False                                                    |
| Ist indiziert             | Richtig                                                     |
| Im globalen Katalog      | Richtig                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| In verwendete Klassen        | [**Verbindungspunkt**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungs Version**](c-applicationversion.md)<br/> [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-Konfiguration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Daten**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | False                                                                                                                    |
| Ist-einwertig       | False                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                     |
| Im globalen Katalog      | Richtig                                                                                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| In verwendete Klassen        | [**ms-DS-Service-Connection-Point-Publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungs Version**](c-applicationversion.md)<br/> [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-Konfiguration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Daten**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungs Version**](c-applicationversion.md)<br/> [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-Konfiguration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Daten**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungs Version**](c-applicationversion.md)<br/> [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-Konfiguration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Daten**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungs Version**](c-applicationversion.md)<br/> [**Verbindungspunkt**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-Konfiguration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Daten**](c-msds-appdata.md)<br/> |



 

 





