---
title: NT-Security-Descriptor-Attribut
description: Die Windows NT-Sicherheitsbeschreibung für das Schemaobjekt. Ein Sicherheitsdeskriptor ist eine Datenstruktur, die Sicherheitsinformationen zu einem Objekt enthält, z. B. den Besitz und die Berechtigungen des Objekts.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- AD-Schema des NT-Security-Descriptor-Attributs
- AD-Schema des nTSecurityDescriptor-Attributs
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33b5753429b63638f1f1c9a3103aa8d78bd8590b77ceebec4fff05b82e10dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703010"
---
# <a name="nt-security-descriptor-attribute"></a>NT-Security-Descriptor-Attribut

Die Windows NT-Sicherheitsbeschreibung für das Schemaobjekt. Ein Sicherheitsdeskriptor ist eine Datenstruktur, die Sicherheitsinformationen zu einem Objekt enthält, z. B. den Besitz und die Berechtigungen des Objekts.

Informationen zum Format dieses Werts finden Sie unter [Security Descriptor String Format (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Eingabe | Wert |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-Descriptor                              |
| Ldap-Anzeigename | Ntsecuritydescriptor                                |
| Size              | \-                                                  |
| Aktualisieren von Berechtigungen  | \-                                                  |
| Updatehäufigkeit  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-Id-Guid    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Is-Single-Valued       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Is-Single-Valued       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | False                                                                                        |
| Is-Single-Valued       | True                                                                                         |
| Ist indiziert             | False                                                                                        |
| Im globalen Katalog      | True                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist einwertig       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist einwertig       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist einwertig       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist einwertig       | True                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | True                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





