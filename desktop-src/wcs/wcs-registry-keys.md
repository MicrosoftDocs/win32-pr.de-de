---
title: WCS-Registrierungsschlüssel
description: WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Farbsystem (WCS), Registrierungsschlüssel
- WCS (Windows Color System), Registrierungsschlüssel
- Imagefarbverwaltung,Registrierungsschlüssel
- Farbverwaltung, Registrierungsschlüssel
- Farben, Registrierungsschlüssel
- WCS-Referenz, Registrierungsschlüssel
- Referenz für WCS, Registrierungsschlüssel
- Windows Farbsystem (WCS), Registrierung
- WCS (Windows Color System), Registrierung
- Imagefarbverwaltung, Registrierung
- Farbverwaltung, Registrierung
- Farben, Registrierung
- WCS-Referenz, Registrierung
- Referenz für WCS, Registrierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c12047d83ccc2f80c26521a59a040fa45df0c21e9bb035efff6ed5d38e8827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814350"
---
# <a name="wcs-registry-keys"></a>WCS-Registrierungsschlüssel

WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofilereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel auf den aktualisierten Zustand des Systemfarbprofils abfragen.

## <a name="active-color-profile-changed"></a>Aktives Farbprofil geändert

Apps möchten möglicherweise auf Farbprofiländerungsereignisse für ein Monitorgerät reagieren. dadurch wird sichergestellt, dass sie immer über genaue Farbinformationen für ihr Ziel verfügen, auch wenn der Benutzer oder eine andere App das aktive Profil für das Gerät geändert hat.

### <a name="desktop-applications"></a>Desktopanwendungen

Desktop-Apps sollten mithilfe von [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)auf Änderungen an der Registrierung lauschen, um zu bestimmen, wann sich farbprofilzuordnungen geändert haben. Eine App sollte sowohl für Benutzerprofil-Zuordnungsänderungen als auch für systemweite Änderungen registriert werden.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) sollte mit einem HKEY initialisiert werden, der von [**RegOpenKeyEx bereitgestellt wird.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) **RegOpenKeyEx** sollte mit den folgenden Registrierungsstruktur-Speicherorten initialisiert werden:



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Zuordnungen pro Benutzerprofil    | **HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion ICM \\ \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}** |
| Systemweite Profilzuordnungen | **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet-Steuerelementklasse \\ \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**                                        |



 

Wenn die App über eine Änderung des Registrierungsschlüssels benachrichtigt wird, sollte sie zunächst abfragen, ob benutzer- oder systemweite Zuordnungen verwendet werden, indem [**wcsGetUsePerUserProfiles aufruft.**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) Anschließend sollte [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) mit dem richtigen [**WCS \_ PROFILE MANAGEMENT \_ \_ SCOPE-Wert**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) aufrufen, um das neue aktive Farbprofil für den Monitor zu erhalten. Beachten Sie, dass nicht alle Änderungen am Registrierungsschlüssel einer tatsächlichen Änderung im derzeit aktiven Farbprofil entsprechen. Die App überprüft, ob sich das von **WcsGetDefaultColorProfile** zurückgegebene Profil tatsächlich geändert hat.

### <a name="universal-windows-uwp-apps"></a>UWP-Apps (Universal Windows)

Universelle Windows-Apps haben keinen Zugriff auf die oben genannten Registrierungsschlüssel. Stattdessen sollten sie einen Handler für das [**DisplayInformation.ColorProfileChanged-Ereignis**](/uwp/api/Windows.Graphics.Display.DisplayInformation) registrieren. Dieses Ereignis wird immer dann angezeigt, wenn sich das aktive Farbprofil für den Monitor geändert hat, auf dem die Anwendung ausgeführt wird. ColorProfileChanged berücksichtigt, ob benutzer- oder systemweite Profilzuordnungen verwendet werden. diese Informationen werden von UWP-Apps abstrahiert.

Wenn auf das ColorProfileChanged-Ereignis reagiert wird, sollte die App das derzeit aktive Profil mithilfe von [**DisplayInformation.GetColorProfileAsync abfragen.**](/uwp/api/Windows.Graphics.Display.DisplayInformation)

 

 