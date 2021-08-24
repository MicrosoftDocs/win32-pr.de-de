---
title: Well-Known-Objects-Attribut
description: Dieses Attribut enthält eine Liste bekannter Objektcontainer nach GUID und Distinguished Name.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- AD-Schema des Well-Known-Objects-Attributs
- wellKnownObjects-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5417b35ef821b1d84377c39eb4408eea57cf0dcc901ae0728a50ba48b88d6779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702410"
---
# <a name="well-known-objects-attribute"></a>Well-Known-Objects-Attribut

Dieses Attribut enthält eine Liste bekannter Objektcontainer nach GUID und Distinguished Name. Die bekannten Objekte sind Systemcontainer. Diese Informationen werden verwendet, um ein Objekt abzurufen, nachdem es verschoben wurde, indem nur die GUID und der Domänenname verwendet werden. Wenn das Objekt verschoben wird, aktualisiert das System automatisch den Distinguished Name-Teil der Well-Known-Objects-Werte, die auf das -Objekt verwiesen haben. Die Datei Ntdsapi.h enthält die folgenden Definitionen, die zum Abrufen eines Objekts verwendet werden können (die GUIDs, die diesen Objekten zugeordnet sind, sind in Ntdsapi.h enthalten):

-   \_GUID-BENUTZERCONTAINER \_ \_ W
-   \_GUID-COMPUTRS-CONTAINER \_ \_ W
-   GUID \_ SYSTEMS \_ CONTAINER \_ W
-   \_GUID-DOMÄNENCONTROLLERCONTAINER \_ \_ \_ W
-   \_GUID-INFRASTRUKTURCONTAINER \_ \_ W
-   GUID \_ DELETED \_ OBJECTS \_ CONTAINER \_ W
-   GUID \_ LOSTANDFOUND \_ CONTAINER \_ W
-   GUID \_ FOREIGNSECURITYPRINCIPALS \_ CONTAINER \_ W
-   \_GUID-PROGRAMMDATENCONTAINER \_ \_ \_ W
-   GUID \_ DES \_ \_ MICROSOFT-PROGRAMMDATENCONTAINERS \_ \_ W
-   GUID \_ NTDS \_ QUOTAS \_ CONTAINER \_ W



| Eingabe | Wert |
|-------------------|-------------------------------------------------|
| CN                | Bekannte Objekte                              |
| Ldap-Anzeigename | wellKnownObjects                                |
| Size              | \-                                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                |
| Updatehäufigkeit  | Jedes Mal, wenn einer der Systemcontainer verschoben wird. |
| Attribute-Id      | 1.2.840.113556.1.4.618                          |
| System-Id-Guid    | 05308983-7688-11d1-aded-00c04fd8d5cd            |
| Syntax            | [**Object(DN-Binary)**](s-object-dn-binary.md) |



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
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Is-Single-Valued       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | True                            |
| Ist einwertig       | False                           |
| Ist indiziert             | False                           |
| Im globalen Katalog      | True                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 16                              |
| Range-Upper            | 16                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





