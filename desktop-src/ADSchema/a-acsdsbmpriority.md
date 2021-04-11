---
title: ACS-DSBM-priority-Attribut
description: Diese Attribute enthalten die Priorität für diesen subnetzbandbreiten-Manager (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-DSBM-Priority-Attributs
- acsdsbmpriority-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd32c9e9cca95dbd5f52569de0b61e886033d13
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123235"
---
# <a name="acs-dsbm-priority-attribute"></a>ACS-DSBM-priority-Attribut

Diese Attribute enthalten die Priorität für diesen subnetzbandbreiten-Manager (SBM). Wenn ein neuer benannter subnetzbandbreiten-Manager (DSBM) ausgewählt werden muss, wird dieser Wert als Teil einer Nachricht zum Bereitstellen von DSBM an andere sbms in der Domäne gesendet \_ . Der SBM mit der höchsten Priorität wird als neue DSBM gewählt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-Priorität                    |
| LDAP-Display-Name | acsdsbmpriority                      |
| Size              | 4 Bytes                              |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-ID-GUID    | 1cb3559e-56d0-11d1-a9c6-0000b80367c1 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
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
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
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
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
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
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
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
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**ACS-Subnetz**](c-acssubnet.md)<br/> |



 

 





