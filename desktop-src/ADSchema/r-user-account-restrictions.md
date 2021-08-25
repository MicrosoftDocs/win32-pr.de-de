---
title: Eigenschaftensatz "Benutzerkonteneinschränkungen"
description: Eigenschaftensatz, der Benutzerattribute enthält, die Kontoeinschränkungen beschreiben.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Ad-Schema für Eigenschaftensatz "Benutzerkonteneinschränkungen"
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050fe70f98bb0bb6fbb457e0540fa61bce9c8f61c2769cf24fb09aa87189d022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702720"
---
# <a name="user-account-restrictions-property-set"></a>Eigenschaftensatz "Benutzerkonteneinschränkungen"

Eigenschaftensatz, der Benutzerattribute enthält, die Kontoeinschränkungen beschreiben.



| Eingabe | Wert |
|--------------|--------------------------------------|
| CN           | Einschränkungen für Benutzerkonten            |
| Anzeigename | Kontoeinschränkungen                 |
| Rechte-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



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
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                             |
| Eigenschaftensatzmember    | [**Ablauf des Kontos**](a-accountexpires.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Eigenschaftensatzmember    | [**Ablauf des Kontos**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                     |
| Eigenschaftensatzmember    | [**Ablauf des Kontos**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Eigenschaftensatzmember    | [**Ablauf des Kontos**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaftensatzmember    | [**Ablauf des Kontos**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaftensatz-Member    | [**Konto läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Account**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Lokalisierungsanzeige-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaftensatz-Member    | [**Konto läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-Computed**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-Last-Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



 

 





