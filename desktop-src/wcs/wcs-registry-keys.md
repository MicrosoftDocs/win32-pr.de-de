---
title: WCS-Registrierungsschlüssel
description: WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofil Ereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel für den aktualisierten Zustand des System Farbprofils Abfragen.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), Registrierungsschlüssel
- WCS (Windows Color System), Registrierungsschlüssel
- Bild Farbverwaltung, Registrierungsschlüssel
- Farbverwaltung, Registrierungsschlüssel
- Farben, Registrierungsschlüssel
- WCS-Referenz, Registrierungsschlüssel
- Referenz für WCs, Registrierungsschlüssel
- Windows Color System (WCS), Registrierung
- WCS (Windows Color System), Registrierung
- Bild Farbverwaltung, Registrierung
- Farbverwaltung, Registrierung
- Farben, Registrierung
- WCS-Referenz, Registrierung
- Referenz für WCs, Registrierung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106373403"
---
# <a name="wcs-registry-keys"></a>WCS-Registrierungsschlüssel

WCS verwendet Registrierungsschlüssel, um zu signalisieren, dass bestimmte Farbprofil Ereignisse aufgetreten sind. Apps sollten diese Registrierungsschlüssel für den aktualisierten Zustand des System Farbprofils Abfragen.

## <a name="active-color-profile-changed"></a>Aktives Farbprofil geändert

Apps können auf das Ändern von Farbprofilen für ein Überwachungsgerät reagieren. Dadurch wird sichergestellt, dass Sie immer über genaue Farbinformationen für Ihr Ziel verfügen, auch wenn der Benutzer oder eine andere APP das aktive Profil für das Gerät geändert hat.

### <a name="desktop-applications"></a>Desktopanwendungen

Desktop-Apps sollten Änderungen an der Registrierung überwachen, um zu bestimmen, wann sich die Zuordnung von Farbprofil Zuordnungen mithilfe von [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)geändert hat. Eine APP sollte sich sowohl für Profil Zuordnungs Änderungen pro Benutzer als auch für systemweite Änderungen registrieren.

[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) muss mit einem HKEY initialisiert werden, der von [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)bereitgestellt wird. **RegOpenKeyEx** muss mithilfe der folgenden Registrierungs Struktur Speicherorte initialisiert werden:



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Profil Zuordnungen pro Benutzer    | **HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ profileassociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}** |
| System weite Profil Zuordnungen | **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**                                        |



 

Wenn die APP über eine Änderung des Registrierungsschlüssels benachrichtigt wird, sollte Sie zuerst Abfragen, ob Benutzer-oder systemweite Zuordnungen durch Aufrufen von [**wcsgetuseperuserprofiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)verwendet werden. Dann sollte [**wcsgetdefaultcolorprofile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) mit dem richtigen Wert für den [**\_ \_ Verwaltungs \_ Bereich des WCS-Profils**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) aufgerufen werden, um das neue aktive Farbprofil für den Monitor zu erhalten. Beachten Sie, dass nicht alle Änderungen des Registrierungsschlüssels einer tatsächlichen Änderung im momentan aktiven Farbprofil entsprechen. die APP Mush prüft, ob das von **wcsgetdefaultcolorprofile** zurückgegebene Profil tatsächlich geändert wurde.

### <a name="universal-windows-uwp-apps"></a>Universelle Windows-Apps (UWP)

Universelle Windows-apps haben keinen Zugriff auf die obigen Registrierungsschlüssel. Stattdessen sollten Sie einen Handler für das [**Display Information. colorprofilechanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) -Ereignis registrieren. Dieses Ereignis wird immer dann ausgelöst, wenn das aktive Farbprofil für den Monitor, auf dem die Anwendung ausgeführt wird, geändert wurde. Colorprofilechanged berücksichtigt, ob Benutzer-oder systemweite Profil Zuordnungen verwendet werden. Diese Informationen werden von UWP-apps abstrahiert.

Wenn Sie auf das colorprofilechanged-Ereignis reagieren, sollte die APP das aktuell aktive Profil mithilfe von " [**Displayinformation. getcolorprofileasync**](/uwp/api/Windows.Graphics.Display.DisplayInformation)" Abfragen.

 

 