---
title: Sam-Account-Type-Attribut
description: Dieses Attribut enthält Informationen zu jedem Kontotyp Objekt.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- AD-Schema des Sam-Account-Type-Attributs
- "\"samAccountType\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957444"
---
# <a name="sam-account-type-attribute"></a>Sam-Account-Type-Attribut

Dieses Attribut enthält Informationen zu jedem Kontotyp Objekt. Sie können eine Liste von Konto Typen auflisten, oder Sie können die API zum Anzeigen von Informationen verwenden, um eine Liste zu erstellen. Da Computer, normale Benutzerkonten und vertrauenswürdige Konten auch als Benutzer Objekte aufgelistet werden können, müssen die Werte für diese Konten ein zusammenhängender Bereich sein.

Die möglichen Werte für dieses Attribut lauten wie folgt:

-   Sam- \_ Domänen \_ Objekt 0x0
-   Sam- \_ Gruppen \_ Objekt 0x10000000
-   Sam \_ - \_ Sicherheits \_ Gruppen \_ Objekt 0x10000001
-   Sam- \_ Alias \_ Objekt 0x20000000
-   Sam \_ - \_ Alias Objekt der nicht Sicherheit \_ \_ 0x20000001
-   Sam- \_ Benutzer \_ Objekt 0x30000000
-   Sam \_ Normal \_ Benutzer \_ Konto 0x30000000
-   Sam- \_ Computer \_ Konto 0x30000001
-   Sam- \_ Vertrauensstellungs \_ Konto 0x30000002
-   Sam- \_ App- \_ Basis \_ Gruppe 0x40000000
-   Sam- \_ App- \_ Abfrage \_ Gruppe 0x40000001
-   Sam \_ - \_ Kontotyp \_ Max 0x7FFFFFFF



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------|
| CN                | Sam-Account-Type                                                |
| LDAP-Display-Name | sAMAccountType                                                  |
| Size              | \-                                                              |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                                |
| Aktualisierungshäufigkeit  | Dies wird vom Betriebssystem festgelegt, wenn das Objekt erstellt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.302                                          |
| System-ID-GUID    | 6e7b626c-64-Dienst-D0-afd2-00c04f 930c9                            |
| Syntax            | [**Enumeration**](s-enumeration.md)                            |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | Richtig                                                         |
| Im globalen Katalog      | Richtig                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



 

 





