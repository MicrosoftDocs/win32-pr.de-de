---
title: User-Logon Eigenschaftensatz
description: Eigenschaftensatz mit Benutzerattributen, die Benutzeranmeldungsinformationen beschreiben.
ms.assetid: 93d1af8d-f4d0-4aed-a03d-a2f34dd7ec37
ms.tgt_platform: multiple
keywords:
- User-Logon des AD-Schemas für den Eigenschaftensatz
topic_type:
- apiref
api_name:
- User-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08b06cb7ccf22f77727a4789a29e2a884a276687a3cc42d348317dcd250e13dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580560"
---
# <a name="user-logon-property-set"></a>User-Logon Eigenschaftensatz

Eigenschaftensatz mit Benutzerattributen, die Benutzeranmeldungsinformationen beschreiben.



| Eingabe | Wert |
|--------------|--------------------------------------|
| CN           | User-Logon                           |
| Anzeigename | Anmeldeinformationen                    |
| Rights-GUID  | 5f202010-79a5-11d0-9020-00c04fc2d4cf |



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
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Eigenschaftensatz-Member    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Home-Drive**](a-homedrive.md)<br/> [**Letzte Abmelde**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Eigenschaftensatz-Member    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Home-Drive**](a-homedrive.md)<br/> [**Letzte Abmelde**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Zeitstempel der letzten Anmeldung**](a-lastlogontimestamp.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> [**Script-Path**](a-scriptpath.md)<br/> [**Benutzerarbeitsstationen**](a-userworkstations.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                |
| Lokalisierungsanzeige-ID | 10                                                                                                                |
| Eigenschaftensatz-Member    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Zeitstempel der letzten Anmeldung**](a-lastlogontimestamp.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Eigenschaftensatz-Member    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Home-Drive**](a-homedrive.md)<br/> [**Letzte Abmelde**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Zeitstempel der letzten Anmeldung**](a-lastlogontimestamp.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> [**Script-Path**](a-scriptpath.md)<br/> [**Benutzerarbeitsstationen**](a-userworkstations.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Eigenschaftensatz-Member    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Startlaufwerk**](a-homedrive.md)<br/> [**Letzte Abmeldung**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Letzter Anmeldezeitstempel**](a-lastlogontimestamp.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> [**Skriptpfad**](a-scriptpath.md)<br/> [**Benutzerarbeitsstationen**](a-userworkstations.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Eigenschaftensatzmember    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Startlaufwerk**](a-homedrive.md)<br/> [**Letzte Abmeldung**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Letzter Anmeldezeitstempel**](a-lastlogontimestamp.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> [**Skriptpfad**](a-scriptpath.md)<br/> [**Benutzerarbeitsstationen**](a-userworkstations.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**Benutzer**](c-user.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Lokalisierungsanzeige-ID | 10                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Eigenschaftensatzmember    | [**Bad-Pwd-Count**](a-badpwdcount.md)<br/> [**Home-Directory**](a-homedirectory.md)<br/> [**Startlaufwerk**](a-homedrive.md)<br/> [**Letzte Abmeldung**](a-lastlogoff.md)<br/> [**Letzte Anmeldung**](a-lastlogon.md)<br/> [**Letzter Anmeldezeitstempel**](a-lastlogontimestamp.md)<br/> [**Anzahl der Anmeldungen**](a-logoncount.md)<br/> [**Anmeldestunden**](a-logonhours.md)<br/> [**Anmeldearbeitsstation**](a-logonworkstation.md)<br/> [**Profilpfad**](a-profilepath.md)<br/> [**Skriptpfad**](a-scriptpath.md)<br/> [**Benutzerarbeitsstationen**](a-userworkstations.md)<br/> |



 

 





