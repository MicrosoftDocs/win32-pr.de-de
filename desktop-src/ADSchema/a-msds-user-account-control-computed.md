---
title: ms-DS-User-Account-Control-berechnetes Attribut
description: die Berechnung von msDS-User-Account-Control ist ähnlich wie userAccountControl, aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht persistent sind.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- "\"ms-DS-User-Account-Control-berechnetes Attribut AD Schema\""
- AD-Schema "msDS-User-Account-Control-berechnetes Attribut"
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106346563"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>ms-DS-User-Account-Control-berechnetes Attribut

die **Berechnung von msDS-User-Account-Control** ist ähnlich wie [**userAccountControl**](a-useraccountcontrol.md), aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht persistent sind. Die berechneten Bits umfassen Folgendes:



| Wert                | Name (in IADs. h definiert)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **UF- \_ Sperre**<br/>                   |
| 0x800000<br/>  | **\_Kennwort ist \_ abgelaufen.**<br/>         |
| 0x4000000<br/> | **\_Konto für partielle \_ geheimen Schlüssel \_**<br/> |
| 0x8000000<br/> | **UF \_ Verwenden von \_ AES- \_ Schlüsseln**<br/>            |



 

Die vollständige Liste der Bits, die [**Benutzerkontensteuerung**](a-useraccountcontrol.md) und somit auch **msDS-User-Account-Control-berechnete** Elemente enthalten können, finden Sie auch auf der Referenzseite für die **Benutzerkontensteuerung** (zugeordnet über das [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) -Flag) oder auf den Referenzseiten der Netzwerkverwaltung für die [**Benutzer \_ Info \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) -Struktur.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Control-berechnet  |
| LDAP-Display-Name | msDS-User-Account-Control-berechnet   |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-ID-GUID    | 2cc4b836-B63-4940-8d23-ea7acf 06af56 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------|
| Link-ID                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | False                                                             |
| Ist-einwertig       | Richtig                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Objekt**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



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
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

