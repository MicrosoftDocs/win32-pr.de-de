---
title: MS-FRS-Topology-Pref-Attribut
description: Das MS-FRS-Topologie-Pref-Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- MS-FRS-Topology-Pref-Attribut AD-Schema
- msfrs-Topology-Pref-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744665"
---
# <a name="ms-frs-topology-pref-attribute"></a>MS-FRS-Topology-Pref-Attribut

Das **MS-FRS-Topologie-Pref-** Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen. Wenn ein FRS-Mitglied der Replikat Gruppe hinzugefügt oder gelöscht wird, werden diese Attribute und Anpassungen an den Verbindungen zwischen den restlichen FRS-Mitgliedern in der Replikat Gruppe vorgenommen.

Gültige Werte für dieses Attribut sind wie folgt.

| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| 1     | FRS \_ rstopologypref- \_ Ring<br/>     |
| 2     | FRS \_ rstopologypref \_ hubgesprochen<br/> |
| 3     | FRS \_ rstopologypref \_ FullMesh<br/> |
| 4     | FRS \_ rstopologypref \_ Benutzer definiert<br/>   |



 



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Topology-Pref                                               |
| LDAP-Display-Name | msfrs-Topology-Pref                                                |
| Size              | \-                                                                 |
| Berechtigung aktualisieren  | Domänen Administrator                                               |
| Aktualisierungshäufigkeit  | Wenn die Replikat Gruppe erstellt oder die bevorzugte Topologie geändert wird. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID-GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



 

 





