---
title: Instance-Type-Attribut
description: Ein Bitfeld, das festlegt, wie das-Objekt auf einem bestimmten Server instanziiert wird.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- AD-Schema für Instance-Type-Attribut
- AD-Schema des instanceType-Attributs
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744833"
---
# <a name="instance-type-attribute"></a>Instance-Type-Attribut

Ein Bitfeld, das festlegt, wie das-Objekt auf einem bestimmten Server instanziiert wird. Der Wert dieses Attributs kann sich bei verschiedenen Replikaten auch dann unterscheiden, wenn die Replikate synchronisiert sind.

Dieses Attribut kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.

| Wert      | BESCHREIBUNG                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Die Kopfzeile des Namens Kontexts.                                                                        |
| 0x00000002 | Dieses Replikat wird nicht instanziiert.                                                                  |
| 0x00000004 | Das Objekt ist in diesem Verzeichnis beschreibbar.                                                          |
| 0x00000008 | Der namens Kontext für dieses Verzeichnis wird in diesem Verzeichnis gespeichert.                                       |
| 0x00000010 | Der namens Kontext wird zum ersten Mal mithilfe der Replikation erstellt. |
| 0x00000020 | Der namens Kontext wird gerade aus dem lokalen DSA entfernt.                          |



 



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| LDAP-Display-Name | instanceType                                   |
| Size              | 4 Bytes.                                       |
| Berechtigung aktualisieren  | Dieser Wert wird vom Schema Administrator festgelegt. |
| Aktualisierungshäufigkeit  | Wenn das Objekt erstellt wird.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Syntax            | [**Enumeration**](s-enumeration.md)           |



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
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | 0x80bd                          |
| System-Only            | Richtig                            |
| Ist-einwertig       | Richtig                            |
| Ist indiziert             | False                           |
| Im globalen Katalog      | Richtig                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



 

 





