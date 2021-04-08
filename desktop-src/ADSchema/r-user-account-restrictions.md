---
title: Benutzerkonto-Einschränkungs Eigenschaft festgelegt
description: Eigenschaften Satz mit Benutzer Attributen, die Konto Einschränkungen beschreiben.
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- Benutzerkonto-Einschränkungs Eigenschaft festlegen des AD-Schemas
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3c39c80c83f321c654e675ccd87950cfd4bcf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957309"
---
# <a name="user-account-restrictions-property-set"></a>Benutzerkonto-Einschränkungs Eigenschaft festgelegt

Eigenschaften Satz mit Benutzer Attributen, die Konto Einschränkungen beschreiben.



| Eingabe | Wert |
|--------------|--------------------------------------|
| CN           | Einschränkungen für Benutzerkonten            |
| Anzeigename | Kontoeinschränkungen                 |
| Rights-GUID  | 4c164200-20c0-11D0-A768-00aa006e0529 |



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
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/>                                                                                                                                                   |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                             |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                     |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                                                                                                                            |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-Benutzer-Kennwort-Ablaufzeit berechnet**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Konto**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-Benutzer-Kennwort-Ablaufzeit berechnet**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**Computer**](c-computer.md)<br/> [**ms-DS-Managed-Service-Konto**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| Lokalisierung-Display-ID | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Eigenschaften Satz Elemente    | [**Konto: läuft ab**](a-accountexpires.md)<br/> [**ms-DS-User-Account-Control-berechnet**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-Benutzer-Kennwort-Ablaufzeit berechnet**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**PWD-letztes Set**](a-pwdlastset.md)<br/> [**Benutzerkontensteuerung**](a-useraccountcontrol.md)<br/> [**Benutzerparameter**](a-userparameters.md)<br/> |



 

 





