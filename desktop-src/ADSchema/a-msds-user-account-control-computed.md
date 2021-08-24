---
title: ms-DS-User-Account-Control-Computed-Attribut
description: msDS-User-Account-Control-Computed ist ähnlich wie userAccountControl, aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht beibehalten werden.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-DS-User-Account-Control-Computed-Attributs
- AD-Schema des msDS-User-Account-Control-Computed-Attributs
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763260"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>ms-DS-User-Account-Control-Computed-Attribut

**msDS-User-Account-Control-Computed** ist ähnlich wie [**userAccountControl,**](a-useraccountcontrol.md)aber der Wert des Attributs kann zusätzliche Bits enthalten, die nicht beibehalten werden. Die berechneten Bits umfassen Folgendes.



| Wert                | Name (definiert in Iads.h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **UF \_ LOCKOUT**<br/>                   |
| 0x800000<br/>  | **\_UF-KENNWORT \_ ABGELAUFEN**<br/>         |
| 0x4000000<br/> | **UF \_ PARTIAL \_ SECRETS \_ ACCOUNT**<br/> |
| 0x8000000<br/> | **\_UF: \_ VERWENDEN VON AES-SCHLÜSSELN \_**<br/>            |



 

Die vollständige Liste der Bits, die [**User-Account-Control**](a-useraccountcontrol.md) und daher **msDS-User-Account-Control-Computed** enthalten können, finden Sie auch auf der Referenzseite **"User-Account-Control"** (zugeordnet durch das [ADSI-Flagset)](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) oder auf den Referenzseiten zur Netzwerkverwaltung für die Struktur [**\_ \_ "Benutzerinformationen 1008".**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008)



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | ms-DS-User-Account-Control-Computed  |
| Ldap-Anzeigename | msDS-User-Account-Control-Computed   |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-Id-Guid    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Is-Single-Valued       | True                                                              |
| Ist indiziert             | False                                                             |
| Im globalen Katalog      | False                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| In verwendete Klassen        | [**ms-DS-Bindable-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
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
| Ist einwertig       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

