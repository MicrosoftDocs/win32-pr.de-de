---
title: Home-Directory-Attribut
description: Das Basisverzeichnis für das Konto.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- AD-Schema für Home-Directory-Attribut
- AD-Schema für Homedirectory-Attribut
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744849"
---
# <a name="home-directory-attribute"></a>Home-Directory-Attribut

Das Basisverzeichnis für das Konto. Wenn [**HOMEDRIVE**](a-homedrive.md) festgelegt ist und einen Laufwerk Buchstaben angibt, muss das **Homedirectory** ein UNC-Pfad sein. Andernfalls ist **Homedirectory** ein voll qualifizierter lokaler Pfad einschließlich des Laufwerk Buchstabens (z. b. Laufwerk Buchstabe ****: \\**_Verzeichnis_* _\\_ * _Ordner_). Dieser Wert kann eine NULL-Zeichenfolge sein.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| LDAP-Display-Name | homedirectory                                                                      |
| Size              | \-                                                                                 |
| Berechtigung aktualisieren  | Domänen Administrator                                                               |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt wird, und immer dann, wenn das Basisverzeichnis geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-ID-GUID    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                        |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Ist-einwertig       | Richtig                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Ist-einwertig       | Richtig                                                                                |
| Ist indiziert             | False                                                                               |
| Im globalen Katalog      | False                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Ist-einwertig       | Richtig                                                                                |
| Ist indiziert             | False                                                                               |
| Im globalen Katalog      | False                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Ist-einwertig       | Richtig                                                                                |
| Ist indiziert             | False                                                                               |
| Im globalen Katalog      | False                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | False                                                                               |
| Ist-einwertig       | Richtig                                                                                |
| Ist indiziert             | False                                                                               |
| Im globalen Katalog      | False                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





