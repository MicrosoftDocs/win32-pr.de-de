---
title: DN-Reference-Update-Attribut
description: Wenn ein Objekt umbenannt wird, wird dieses Attribut verwendet, um alle vorherigen und aktuellen Namen nachzuverfolgen, die einem Objekt zugewiesen wurden, damit verknüpfte Objekte es weiterhin finden können.
ms.assetid: 28e02a38-eed8-475c-a381-145857477ec6
ms.tgt_platform: multiple
keywords:
- AD-Schema des DN-Reference-Update-Attributs
- dNReferenceUpdate-Attribut AD-Schema
topic_type:
- apiref
api_name:
- DN-Reference-Update
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ba8c11b97a3fede86c2ba14a8f331438573b8587fe760fb550ee7d707e8354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177536"
---
# <a name="dn-reference-update-attribute"></a>DN-Reference-Update-Attribut

Wenn ein Objekt umbenannt wird, wird dieses Attribut verwendet, um alle vorherigen und aktuellen Namen nachzuverfolgen, die einem Objekt zugewiesen wurden, damit verknüpfte Objekte es weiterhin finden können.



| Eingabe | Wert |
|-------------------|-----------------------------------------|
| CN                | DN-Reference-Update                     |
| Ldap-Anzeigename | dNReferenceUpdate                       |
| Size              | \-                                      |
| Aktualisieren von Berechtigungen  | Dies wird vom System festgelegt.              |
| Updatehäufigkeit  | \-                                      |
| Attribute-Id      | 1.2.840.113556.1.4.1242                 |
| System-ID-GUID    | 2df90d86-009f-11d2-aa4c-00c04fd7d83a    |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | True                                                               |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Richtig                                                               |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Richtig                                                               |
| Ist einwertig       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Richtig                                                               |
| Is-Single-Valued       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | Richtig                                                               |
| Is-Single-Valued       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------------|
| Link-ID                | \-                                                                 |
| MAPI-Id                | \-                                                                 |
| System-Only            | True                                                               |
| Is-Single-Valued       | Falsch                                                              |
| Ist indiziert             | Falsch                                                              |
| Im globalen Katalog      | Falsch                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000008                                                         |
| System-Flags           | 0x00000010                                                         |
| In verwendete Klassen        | [**Infrastructure-Update**](c-infrastructureupdate.md)<br/> |



 

 





