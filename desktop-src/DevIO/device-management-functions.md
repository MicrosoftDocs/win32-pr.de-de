---
description: Die folgenden Funktionen werden in der Geräteverwaltung verwendet.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Geräte Verwaltungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958334"
---
# <a name="device-management-functions"></a>Geräte Verwaltungsfunktionen

Die folgenden Funktionen werden in der Geräteverwaltung verwendet.



| Funktion                                                             | BESCHREIBUNG                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Sendet einen Steuerungs Code direkt an einen angegebenen Gerätetreiber.                           |
| [**Installnewdevice**](installnewdevice.md)                         | Installiert ein neues Gerät. Der Benutzer wird aufgefordert, das Gerät auszuwählen.                     |
| [**Registerdevicenotifizierung**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Registriert das Gerät oder den Typ des Geräts, für das ein Fenster Benachrichtigungen empfängt. |
| [**Unregisterdevicenotifizierung**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Schließt das angegebene Benachrichtigungs Handle des Geräts.                                      |



 

Die folgenden Funktionen werden mit CD-ROM-und DVD-Laufwerken verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Cdromdisabledigitalplayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Deaktiviert die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk.                                    |
| [**Cdromenabledigitalplayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Aktiviert die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk.                                     |
| [**Cdromisdigitalplaybackaktivierte**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Bestimmt, ob die digitale Wiedergabe für das angegebene CD-ROM-oder DVD-Laufwerk aktiviert ist.               |
| [**Cdromknowngooddigitalplayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Bestimmt, ob das angegebene CD-ROM-oder DVD-Laufwerk eine digitale Wiedergabe aufweist, die bekanntermaßen gut ist. |
| [**DVDLauncher**](dvdlauncher.md)                                     | Überprüft, ob der Medienbereich im DVD-Laufwerk mit dem DVD-Laufwerks Bereich übereinstimmt.                       |



 

 

 
