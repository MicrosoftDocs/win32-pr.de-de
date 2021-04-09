---
title: Parent-GUID-Attribut
description: Dies ist ein konstruiertes Attribut, das zur Unterstützung des Dirsync-Steuer Elements erfunden wurde. Dieses Attribut enthält die objectGUID des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- AD-Schema für Parent-GUID-Attribut
- cschema für das Attribut "parametriguid"
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859784"
---
# <a name="parent-guid-attribute"></a>Parent-GUID-Attribut

Dies ist ein konstruiertes Attribut, das zur Unterstützung des Dirsync-Steuer Elements erfunden wurde. Dieses Attribut enthält die objectGUID des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Parent-GUID                                           |
| LDAP-Display-Name | parametriguid                                            |
| Size              | 16 Bytes                                              |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                      |
| Aktualisierungshäufigkeit  | Während der Replikation                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID-GUID    | 2df90d74-009F -11d2-aa4c-00c04f d83a                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist-einwertig       | Richtig         |
| Ist indiziert             | False        |
| Im globalen Katalog      | False        |
| NT-Security-Descriptor | o:Bag: schlecht: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



 

 




