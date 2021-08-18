---
description: Die folgenden Funktionen werden in der Geräteverwaltung verwendet.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Geräteverwaltung Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a648fb5141d9efa977e573e3b0abb32fe6c504f11647a2dc392e9838da63ca6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956899"
---
# <a name="device-management-functions"></a>Geräteverwaltung Functions

Die folgenden Funktionen werden in der Geräteverwaltung verwendet.



| Funktion                                                             | Beschreibung                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Sendet einen Steuerungscode direkt an einen angegebenen Gerätetreiber.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registriert das Gerät oder den Gerätetyp, für das ein Fenster Benachrichtigungen erhält. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Schließt das angegebene Gerätebenachrichtigungshand handle.                                      |



 

Die folgenden Funktionen werden mit CD-ROM- und DVD-Laufwerken verwendet.



| Funktion                                                               | Beschreibung                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CodiDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Deaktiviert die digitale Wiedergabe für das angegebene CD-ROM- oder DVD-Laufwerk.                                    |
| [**C skriptfähigesDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Aktiviert die digitale Wiedergabe für das angegebene CD-ROM- oder DVD-Laufwerk.                                     |
| [**ComeIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Bestimmt, ob die digitale Wiedergabe für das angegebene CD-ROM- oder DVD-Laufwerk aktiviert ist.               |
| [**CodiKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Bestimmt, ob das angegebene CD-ROM- oder DVD-Laufwerk über eine als gut bekannte digitale Wiedergabe verfügt. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Überprüft, ob der Medienbereich auf dem DVD-Laufwerk dem DVD-Laufwerksbereich entspricht.                       |



 

 

 
