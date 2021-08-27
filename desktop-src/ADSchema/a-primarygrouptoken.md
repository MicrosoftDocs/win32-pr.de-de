---
title: Primary-Group-Token-Attribut
description: Ein berechnetes Attribut, das zum Abrufen der Mitgliedschaftsliste einer Gruppe verwendet wird, z. B. Domänenbenutzer. Die vollständige Mitgliedschaft solcher Gruppen wird aus Skalierungsgründen nicht explizit gespeichert.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- AD-Schema des Attributs "Primary-Group-Token"
- PRIMARYGROUPToken-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd83e89a25a81f6d62207e48053fff5cafd279e29b482a9b80cb02de580ad3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065920"
---
# <a name="primary-group-token-attribute"></a>Primary-Group-Token-Attribut

Ein berechnetes Attribut, das zum Abrufen der Mitgliedschaftsliste einer Gruppe verwendet wird, z. B. Domänenbenutzer. Die vollständige Mitgliedschaft solcher Gruppen wird aus Skalierungsgründen nicht explizit gespeichert.



| Eingabe | Wert |
|-------------------|--------------------------------------------|
| CN                | Primäres Gruppentoken                        |
| Ldap-Anzeigename | primaryGroupToken                          |
| Size              | 4 Bytes                                    |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.           |
| Updatehäufigkeit  | Wenn sich eine primäre Objektgruppe ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntax            | [**Enumeration**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist einwertig       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist einwertig       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Ist einwertig       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Is-Single-Valued       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Is-Single-Valued       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Is-Single-Valued       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------|
| Link-ID                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Richtig                                |
| Is-Single-Valued       | Richtig                                |
| Ist indiziert             | Falsch                               |
| Im globalen Katalog      | Falsch                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> |



 

 





