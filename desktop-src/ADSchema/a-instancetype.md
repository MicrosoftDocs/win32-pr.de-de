---
title: Instance-Type-Attribut
description: Ein Bitfeld, das vorgibt, wie das Objekt auf einem bestimmten Server instanziiert wird.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Instance-Type AD-Attributschema
- instanceType-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb087afedfb6570c2d25858ca99a53749607f2260f3a6f7a24ae766e22ea3e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925280"
---
# <a name="instance-type-attribute"></a>Instance-Type-Attribut

Ein Bitfeld, das vorgibt, wie das Objekt auf einem bestimmten Server instanziiert wird. Der Wert dieses Attributs kann sich auf verschiedenen Replikaten unterscheiden, auch wenn die Replikate synchron sind.

Dieses Attribut kann 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte sein.

| Wert      | Beschreibung                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Der Haupthaupt des Namenskontexts.                                                                        |
| 0x00000002 | Dieses Replikat wird nicht instanziiert.                                                                  |
| 0x00000004 | Das -Objekt kann in diesem Verzeichnis geschrieben werden.                                                          |
| 0x00000008 | Der Namenskontext oberhalb dieses Namens in diesem Verzeichnis wird gespeichert.                                       |
| 0x00000010 | Der Namenskontext wird gerade zum ersten Mal mithilfe der Replikation erstellt. |
| 0x00000020 | Der Namenskontext wird gerade aus dem lokalen DSA entfernt.                          |



 



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| Ldap-Anzeigename | instanceType                                   |
| Size              | 4 Bytes.                                       |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom Schemaadministrator festgelegt. |
| Updatehäufigkeit  | Wenn das Objekt erstellt wird.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Syntax            | [**Enumeration**](s-enumeration.md)           |



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
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Richtig                            |
| Ist einwertig       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





