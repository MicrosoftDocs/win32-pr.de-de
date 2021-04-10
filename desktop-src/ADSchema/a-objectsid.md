---
title: Object-Sid-Attribut
description: Ein binärer Wert, der die Sicherheits-ID (SID) des Benutzers angibt. Die SID ist ein eindeutiger Wert, der verwendet wird, um den Benutzer als Sicherheits Prinzipal zu identifizieren.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- AD-Schema für Object-Sid-Attribut
- AD-Schema des objectSID-Attributs
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b536650177f873cbbc349096e84c3de274b8d376
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107637"
---
# <a name="object-sid-attribute"></a>Object-Sid-Attribut

Ein binärer Wert, der die Sicherheits-ID (SID) des Benutzers angibt. Die SID ist ein eindeutiger Wert, der verwendet wird, um den Benutzer als Sicherheits Prinzipal zu identifizieren.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| LDAP-Display-Name | objectSid                                                    |
| Size              | \-                                                           |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                             |
| Aktualisierungshäufigkeit  | Dieser Wert wird vom System festgelegt, wenn das Konto erstellt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-ID-GUID    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Syntax            | [**Zeichenfolge (SID)**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Richtig                                                                                                                                                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | Richtig                                                                                                                                                                                             |
| Ist-einwertig       | Richtig                                                                                                                                                                                             |
| Ist indiziert             | Richtig                                                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**ms-DS-BIND-Proxy**](c-msds-bindproxy.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Richtig                                                                                                                                                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Richtig                                                                                                                                                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Richtig                                                                                                                                                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Richtig                                                                                                                                                                                                                                                       |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                       |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                       |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**Fremd Sicherheits Prinzipal**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migriert-Benutzer**](c-msmqmigrateduser.md)<br/> [**SAM-Domain-Base**](c-samdomainbase.md)<br/> [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



 

 





