---
title: ATTRIBUT "ACS-DSBM-Priority"
description: Diese Attribute enthalten die Priorität für diesen Subnetzbandbreiten-Manager (SBM).
ms.assetid: 08dd49d2-a2fa-4707-8302-25566680b91d
ms.tgt_platform: multiple
keywords:
- AD-Schema des ACS-DSBM-Priority-Attributs
- aCSDSBMPriority-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ACS-DSBM-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7a80c9c866b5c91f83f884ecaafe60e4596af4ca8d625791ed9264679c356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637490"
---
# <a name="acs-dsbm-priority-attribute"></a>ATTRIBUT "ACS-DSBM-Priority"

Diese Attribute enthalten die Priorität für diesen Subnetzbandbreiten-Manager (SBM). Wenn ein neuer Designated Subnet Bandwidth Manager (DSBM) ausgewählt werden muss, wird dieser Wert als Teil einer DSBM-Bereitschaftsnachricht an andere SBMs in der Domäne \_ gesendet. Sbm mit der höchsten Priorität wird als neues DSBM gewählt.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ACS-DSBM-Priority                    |
| Ldap-Anzeigename | aCSDSBMPriority                      |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.776               |
| System-ID-GUID    | 1cb3559e-56d0-11d1-a9c6-0000f80367c1 |
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



 

 





