---
title: Parent-GUID-Attribut
description: Dies ist ein konstruiertes Attribut, das zur Unterstützung des DirSync-Steuerelements konzipiert ist. Dieses Attribut enthält objectGuid des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- AD-Schema des Parent-GUID-Attributs
- parentGUID-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f42ba5aedc73f04d8967b84bcfbff39c54ce0dbcdf769e48a747ffa0d3e8c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119325430"
---
# <a name="parent-guid-attribute"></a>Parent-GUID-Attribut

Dies ist ein konstruiertes Attribut, das zur Unterstützung des DirSync-Steuerelements konzipiert ist. Dieses Attribut enthält objectGuid des übergeordneten Elements eines Objekts beim Replizieren der Erstellung, Umbenennung oder Verschiebung eines Objekts.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Übergeordnete GUID                                           |
| Ldap-Anzeigename | parentGUID                                            |
| Size              | 16 Bytes                                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                      |
| Updatehäufigkeit  | Während der Replikation                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID-GUID    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------|
| Link-ID                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Richtig         |
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
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
| Ist einwertig       | Richtig         |
| Ist indiziert             | Falsch        |
| Im globalen Katalog      | Falsch        |
| NT-Security-Descriptor | O:BAG:BAD:S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| In verwendete Klassen        | \-           |



 

 




