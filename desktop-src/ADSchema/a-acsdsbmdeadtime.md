---
title: ACS-DSBM-DeadTime-Attribut
description: Dieses Attribut enthält das wahllose Zeitintervall (DSBMDeadInterval) für eine Domäne.
ms.assetid: c3a0780c-1786-4631-b870-77146de87f18
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-DSBM-DeadTime-Attributs
- aCSDSBMDeadTime-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-DeadTime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a58c46cb4497e7967e21810acaeed590d022d75e0d1312bf8d6522ec3ba5949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022928"
---
# <a name="acs-dsbm-deadtime-attribute"></a>ACS-DSBM-DeadTime-Attribut

Dieses Attribut enthält das wahllose Zeitintervall (DSBMDeadInterval) für eine Domäne. Wenn der Designierte Subnetzbandbreiten-Manager \_ während dieses Intervalls keine I AM \_ DSBM-Ankündigung sendet, wählen die anderen Subnetzbandbreiten-Manager (SBMs) in der Domäne eine neue DSBM aus.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-DeadTime                    |
| Ldap-Anzeigename | aCSDSBMDeadTime                      |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.778               |
| System-ID-GUID    | 1cb355a0-56d0-11d1-a9c6-0000f80367c1 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



 

 





