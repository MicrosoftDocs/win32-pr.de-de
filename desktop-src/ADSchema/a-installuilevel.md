---
title: Install-Attribute auf Benutzeroberflächen Ebene
description: Dieses Attribut enthält Informationen für den Typ (Ebene) der Installation, die für die Benutzeroberfläche verwendet wird.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- AD-Schema für die Installation auf Benutzeroberflächen Ebene
- AD-Schema des installuilevel-Attributs
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957338"
---
# <a name="install-ui-level-attribute"></a>Install-Attribute auf Benutzeroberflächen Ebene

Dieses Attribut enthält Informationen für den Typ (Ebene) der Installation, die für die Benutzeroberfläche verwendet wird. Folgende Installations Ebenen sind möglich: 2 installuilevel \_ None (unbeaufsichtigte Installation) 3 installuilevel \_ Basic (einfache Installation mit Fehlerbehandlung) 4 installuilevel \_ Reduced (erstellte Benutzeroberfläche, unterdrückte Dialogfelder für Assistenten) 5 installuilevel \_ Full (erstellte Benutzeroberfläche mit Assistenten, Status, Fehler)



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Install-UI-Level                     |
| LDAP-Display-Name | installuilevel                       |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.847               |
| System-ID-GUID    | 96a7dd64-9118-11d1-AEbc-0000f 80367c1 |
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
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------|
| Link-ID                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Ist-einwertig       | Richtig                                                             |
| Ist indiziert             | False                                                            |
| Im globalen Katalog      | False                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| In verwendete Klassen        | [**Paket Registrierung**](c-packageregistration.md)<br/> |



 

 





