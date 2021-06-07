---
title: WCS-Registrierungsschlüssel
description: WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), Registrierungsschlüssel
- WCS (Windows Color System), Registrierungsschlüssel
- Bildfarbverwaltung, Registrierungsschlüssel
- Farbverwaltung, Registrierungsschlüssel
- Farben, Registrierungsschlüssel
- WCS-Referenz, Registrierungsschlüssel
- Referenz für WCS, Registrierungsschlüssel
- Windows Color System (WCS),Registrierung
- WCS (Windows-Farbsystem),Registrierung
- Bildfarbverwaltung,Registrierung
- Farbverwaltung,Registrierung
- Farben, Registrierung
- WCS-Referenz,Registrierung
- Referenz für WCS, Registrierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444671"
---
# <a name="wcs-registry-keys"></a>WCS-Registrierungsschlüssel

WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.

## <a name="active-color-profile-changed"></a>Aktives Farbprofil geändert

Apps möchten möglicherweise auf Farbprofiländerungsereignisse für ein Überwachungsgerät reagieren. Dadurch wird sichergestellt, dass sie immer über genaue Farbinformationen für ihr Ziel verfügen, auch wenn der Benutzer oder eine andere App das aktive Profil für das Gerät geändert hat.

### <a name="desktop-applications"></a>Desktopanwendungen

Desktop-Apps sollten mithilfe von [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)auf Änderungen an der Registrierung lauschen, um zu bestimmen, wann sich eine Farbprofilzuordnung geändert hat. Eine App sollte sowohl für Benutzerprofilzuordnungsänderungen als auch für systemweite Änderungen registriert werden.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) sollte mit einem von [**RegOpenKeyEx bereitgestellten**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)HKEY initialisiert werden. **RegOpenKeyEx** sollte mit den folgenden Registrierungsstrukturspeicherorten initialisiert werden:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Benutzerspezifische Profilzuordnungen    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Systemweite Profilzuordnungen | **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Class \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Wenn die App über eine Änderung des Registrierungsschlüssels benachrichtigt wird, sollte sie zuerst abfragen, ob benutzer- oder systemweite Zuordnungen durch Aufrufen von [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)verwendet werden. Anschließend sollte [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) mit dem richtigen [**WCS \_ PROFILE MANAGEMENT \_ \_ SCOPE-Wert**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) aufgerufen werden, um das neue aktive Farbprofil für den Monitor abzurufen. Beachten Sie, dass nicht alle Änderungen des Registrierungsschlüssels einer tatsächlichen Änderung im derzeit aktiven Farbprofil entsprechen. Die App überprüft, ob sich das von **WcsGetDefaultColorProfile** zurückgegebene Profil tatsächlich geändert hat.

### <a name="universal-windows-uwp-apps"></a>Universelle Windows-Apps (UWP)

Universelle Windows-Apps haben keinen Zugriff auf die oben genannten Registrierungsschlüssel. Stattdessen sollten sie einen Handler für das [**DisplayInformation.ColorProfileChanged-Ereignis**](/uwp/api/Windows.Graphics.Display.DisplayInformation) registrieren. Dieses Ereignis wird immer dann ausgelöst, wenn sich das aktive Farbprofil für den Monitor, auf dem die Anwendung ausgeführt wird, geändert hat. ColorProfileChanged berücksichtigt, ob benutzer- oder systemweite Profilzuordnungen verwendet werden. Diese Informationen werden von UWP-Apps abstrahiert.

Wenn sie auf das ColorProfileChanged-Ereignis reagiert, sollte die App das derzeit aktive Profil mit [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation)abfragen.

 

 