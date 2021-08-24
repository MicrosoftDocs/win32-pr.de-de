---
title: Time-Refresh-Attribut
description: Dieses Attribut verfügt über das Intervall, in dem ein Ressourcendatensatz, der in einer integrierten Active Directory-Zone enthalten ist, für den DNS-Server aktualisiert werden soll. Das Standardintervall beträgt 7 Tage.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- Time-Refresh AD-Schema
- ad-Schema des timeRefresh-Attributs
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27705c55e3d16003bc40bfb72c3bf9d0b06260e239aa0c83dbd4e05a484dbc1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704070"
---
# <a name="time-refresh-attribute"></a>Time-Refresh-Attribut

Dieses Attribut verfügt über das Intervall, in dem ein Ressourcendatensatz, der in einer integrierten Active Directory-Zone enthalten ist, für den DNS-Server aktualisiert werden soll. Das Standardintervall beträgt 7 Tage.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Time-Refresh                         |
| Ldap-Anzeigename | timeRefresh                          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.503               |
| System-Id-Guid    | ddac0cf1-af8f-11d0-afeb-00c04fd930c9 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Is-Single-Valued       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Is-Single-Valued       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Is-Single-Valued       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist einwertig       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist einwertig       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist einwertig       | True                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



 

 





