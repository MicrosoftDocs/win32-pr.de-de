---
title: NT-Security-Descriptor-Attribut
description: Der Windows NT-Sicherheits Deskriptor für das Schema Objekt. Eine Sicherheits Beschreibung ist eine Datenstruktur, die Sicherheitsinformationen zu einem Objekt enthält, z. b. den Besitz und die Berechtigungen des Objekts.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- NT-Security-Descriptor-Attribut, AD-Schema
- AD-Schema des ntSecurityDescriptor-Attributs
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e951e28ce97b04380609774baf57e4c6bf8c545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519711"
---
# <a name="nt-security-descriptor-attribute"></a>NT-Security-Descriptor-Attribut

Der Windows NT-Sicherheits Deskriptor für das Schema Objekt. Eine Sicherheits Beschreibung ist eine Datenstruktur, die Sicherheitsinformationen zu einem Objekt enthält, z. b. den Besitz und die Berechtigungen des Objekts.

Weitere Informationen zum Format dieses Werts finden Sie unter [Sicherheits Deskriptor-Zeichen folgen Format (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Eingabe | Wert |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-Descriptor                              |
| LDAP-Display-Name | ntSecurityDescriptor                                |
| Size              | \-                                                  |
| Berechtigung aktualisieren  | \-                                                  |
| Aktualisierungshäufigkeit  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-ID-GUID    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001a                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | False                                                                                        |
| Ist-einwertig       | Richtig                                                                                         |
| Ist indiziert             | False                                                                                        |
| Im globalen Katalog      | Richtig                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001a                                                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001a                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001a                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001a                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | False                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                               |
| Ist indiziert             | False                                                                                                                                              |
| Im globalen Katalog      | Richtig                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001a                                                                                                                                         |
| In verwendete Klassen        | [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





