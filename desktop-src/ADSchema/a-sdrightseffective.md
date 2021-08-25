---
title: SD-Rights-Effective-Attribut
description: 'Dieses konstruierte Attribut gibt einen einzelnen DWORD-Wert zurück, für den bis zu drei Bits festgelegt werden können: OWNER \_ SECURITY \_ INFORMATIONDACL \_ SECURITY \_ INFORMATIONSACL \_ SECURITY INFORMATION Wenn ein Bit festgelegt \_ ist, hat der Benutzer Schreibzugriff auf den entsprechenden Teil der Sicherheitsbeschreibung. Besitzer bedeutet sowohl Besitzer als auch Gruppe.'
ms.assetid: 66d1aefb-49be-42fc-b144-3fb95c59dd0f
ms.tgt_platform: multiple
keywords:
- AD-Schema des SD-Rights-Effective-Attributs
- sDRightsEffective-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- SD-Rights-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d65591c935955133ca004c066249e9c6ec4a2effa102ad8b0e2650e6e5155749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923220"
---
# <a name="sd-rights-effective-attribute"></a>SD-Rights-Effective-Attribut

Dieses konstruierte Attribut gibt einen einzelnen **DWORD-Wert** zurück, für den bis zu drei Bits festgelegt werden können:

-   \_ \_ BESITZERSICHERHEITSINFORMATIONEN
-   \_DACL-SICHERHEITSINFORMATIONEN \_
-   \_SACL-SICHERHEITSINFORMATIONEN \_

Wenn ein Bit festgelegt ist, hat der Benutzer Schreibzugriff auf den entsprechenden Teil der Sicherheitsbeschreibung. Besitzer bedeutet sowohl Besitzer als auch Gruppe.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | SD-Rights-Effective                  |
| Ldap-Anzeigename | sDRightsEffective                    |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1304              |
| System-ID-GUID    | c3dbafa6-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | False                           |
| Ist einwertig       | True                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | False                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x08000014                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





