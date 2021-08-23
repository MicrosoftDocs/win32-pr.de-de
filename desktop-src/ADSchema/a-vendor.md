---
title: Vendor-Attribut
description: Dieses Attribut identifiziert den Anbieter für eine Anwendung.
ms.assetid: af376e9a-ae30-49f5-baff-c888e83688b0
ms.tgt_platform: multiple
keywords:
- Anbieterattribut AD-Schema
- Anbieterattribut AD-Schema
topic_type:
- apiref
api_name:
- Vendor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69521e58a26ec2b3bf081f9674c857c04339db4a2b9f0f524589c89868d1462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702630"
---
# <a name="vendor-attribute"></a>Vendor-Attribut

Dieses Attribut identifiziert den Anbieter für eine Anwendung.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Hersteller                                      |
| Ldap-Anzeigename | vendor                                      |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.255                      |
| System-ID-GUID    | 281416df-1968-11d0-a28f-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist einwertig       | True                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 512                                                              |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paketregistrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                   |
| Ist einwertig       | True                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungsversion**](c-applicationversion.md)<br/> [**Paketregistrierung**](c-packageregistration.md)<br/> [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                   |
| Ist einwertig       | True                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungsversion**](c-applicationversion.md)<br/> [**Paketregistrierung**](c-packageregistration.md)<br/> [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungsversion**](c-applicationversion.md)<br/> [**Paketregistrierung**](c-packageregistration.md)<br/> [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungsversion**](c-applicationversion.md)<br/> [**Paketregistrierung**](c-packageregistration.md)<br/> [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                   |
| Is-Single-Valued       | True                                                                                                                                                                                                    |
| Ist indiziert             | False                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                            |
| Range-Lower            | 0                                                                                                                                                                                                       |
| Range-Upper            | 512                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                              |
| In verwendete Klassen        | [**Anwendungsversion**](c-applicationversion.md)<br/> [**Paketregistrierung**](c-packageregistration.md)<br/> [**Dienstverbindungspunkt**](c-serviceconnectionpoint.md)<br/> |



 

 





