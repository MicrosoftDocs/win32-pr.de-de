---
title: ms-DS-Az-Biz-Rule-Attribut
description: Der Text des Skripts, das die Geschäftsregel implementieren soll.
ms.assetid: 884513ae-9600-49b0-a371-6f77b84b54f9
ms.tgt_platform: multiple
keywords:
- MS-DS-Az-Biz-Rule-Attribut AD-Schema
- AD-Schema des msDS-AzBizRule-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Az-Biz-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 215afa79e47a1ddf508b3d9d7a3d646c3157bafec4716eac31fae6b4b733058e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118685370"
---
# <a name="ms-ds-az-biz-rule-attribute"></a>ms-DS-Az-Biz-Rule-Attribut

Der Text des Skripts, das die Geschäftsregel implementieren soll.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-DS-Az-Biz-Rule                           |
| Ldap-Anzeigename | msDS-AzBizRule                              |
| Size              | 128 Zeichen                              |
| Aktualisieren von Berechtigungen  | AzRoles admin                               |
| Updatehäufigkeit  | Während der Initialisierung oder Richtlinienänderung.     |
| Attribute-Id      | 1.2.840.113556.1.4.1801                     |
| System-Id-Guid    | 33d41ea8-c0c9-4c92-9494-f104878413fd        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------|
| Link-ID                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falsch                                             |
| Is-Single-Valued       | Richtig                                              |
| Ist indiziert             | Falsch                                             |
| Im globalen Katalog      | Falsch                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                      |
| Range-Lower            | 0                                                 |
| Range-Upper            | 65536                                             |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000010                                        |
| In verwendete Klassen        | [**ms-DS-Az-Task**](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------|
| Link-ID                | \-                                                |
| MAPI-Id                | \-                                                |
| System-Only            | Falsch                                             |
| Is-Single-Valued       | Richtig                                              |
| Ist indiziert             | Falsch                                             |
| Im globalen Katalog      | Falsch                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                      |
| Range-Lower            | 0                                                 |
| Range-Upper            | 65536                                             |
| Search-Flags           | 0x00000000                                        |
| System-Flags           | 0x00000010                                        |
| In verwendete Klassen        | [**ms-DS-Az-Task**](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | 0                                                                                     |
| Range-Upper            | 65536                                                                                 |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**ms-DS-Az-Task**](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Ist einwertig       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | 0                                                                                     |
| Range-Upper            | 65536                                                                                 |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**ms-DS-Az-Task**](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Ist einwertig       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | 0                                                                                     |
| Range-Upper            | 65536                                                                                 |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**ms-DS-Az-Task**](c-msds-aztask.md)<br/> |



 

 





