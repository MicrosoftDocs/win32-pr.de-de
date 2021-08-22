---
title: ms-FRS-Topology-Pref-Attribut
description: Das attribut ms-FRS-Topology-Pref wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen zu erfassen.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-FRS-Topology-Pref-Attributs
- AD-Schema des msFRS-Topology-Pref-Attributs
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8467a038db4f5c263253d31c33cb7dc01bb548712918d654b27b7778079d5c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960529"
---
# <a name="ms-frs-topology-pref-attribute"></a>ms-FRS-Topology-Pref-Attribut

Das **attribut ms-FRS-Topology-Pref** wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen zu erfassen. Wenn ein FRS-Mitglied der Replikatgruppe hinzugefügt oder gelöscht wird, werden auf diese Attribute verwiesen, und es werden Anpassungen an den Verbindungen zwischen den restlichen FRS-Membern in der Replikatgruppe vorgenommen.

Gültige Werte für dieses Attribut sind:

| Wert | Beschreibung                              |
|-------|------------------------------------------|
| 1     | FRS \_ RSTOPOLOGYPREF \_ RING<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | FRS \_ RSTOPOLOGYPREF \_ CUSTOM<br/>   |



 



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Topology-Pref                                               |
| Ldap-Anzeigename | msFRS-Topology-Pref                                                |
| Size              | \-                                                                 |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                               |
| Updatehäufigkeit  | Wenn die Replikatgruppe erstellt wird oder sich die bevorzugte Topologie ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-Id-Guid    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Ist einwertig       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Ist einwertig       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



 

 





