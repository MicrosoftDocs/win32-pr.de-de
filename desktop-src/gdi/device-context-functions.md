---
description: Die folgenden Funktionen werden mit Gerätekontexten verwendet.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Gerätekontextfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33eda03ce65a5873c4420f6675128243e30493dc75fa3055c8718f6826f4a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966050"
---
# <a name="device-context-functions"></a>Gerätekontextfunktionen

Die folgenden Funktionen werden mit Gerätekontexten verwendet.



| Funktion                                                   | Beschreibung                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Bricht alle ausstehenden Vorgänge im angegebenen Gerätekontext ab.                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Ändert die Einstellungen des Standardanzeigegeräts in den angegebenen Grafikmodus.                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Ändert die Einstellungen des angegebenen Anzeigegeräts in den angegebenen Grafikmodus.                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Erstellt einen Speichergerätekontext, der mit dem angegebenen Gerät kompatibel ist.                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Erstellt einen Gerätekontext für ein Gerät unter Verwendung des angegebenen Namens.                                                                           |
| [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Erstellt einen Informationskontext für das angegebene Gerät.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Löscht den angegebenen Gerätekontext.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Löscht einen logischen Stift, Pinsel, eine Schriftart, eine Bitmap, einen Bereich oder eine Palette und gibt alle Systemressourcen frei, die dem -Objekt zugeordnet sind.                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Ruft die Funktionen eines Druckergerätetreibers ab.                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Stellt Zeichnungsfunktionen der angegebenen Videoanzeige bereit, die nicht direkt über die Grafikgeräteschnittstelle verfügbar sind.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Ruft Informationen zu den Anzeigegeräten in einem System ab.                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Ruft Informationen zu einem der Grafikmodi für ein Anzeigegerät ab.                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Ruft Informationen zu einem der Grafikmodi für ein Anzeigegerät ab.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Listet die Stifte oder Pinsel auf, die für den angegebenen Gerätekontext verfügbar sind.                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Eine anwendungsdefinierte Rückruffunktion, die mit der [**EnumObjects-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) verwendet wird.                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Ruft ein Handle für ein Objekt des angegebenen Typs ab, das im angegebenen Gerätekontext ausgewählt wurde.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Ruft ein Handle für einen Anzeigegerätekontext für den Clientbereich eines angegebenen Fensters oder für den gesamten Bildschirm ab.                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Ruft die aktuelle Pinselfarbe für den angegebenen Gerätekontext ab.                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Ruft ein Handle für einen Anzeigegerätekontext für den Clientbereich eines angegebenen Fensters oder für den gesamten Bildschirm ab.                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Ruft den endgültigen Übersetzungsursprung für einen angegebenen Gerätekontext ab.                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Ruft die aktuelle Stiftfarbe für den angegebenen Gerätekontext ab.                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Ruft gerätespezifische Informationen für das angegebene Gerät ab.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Ruft das Layout eines Gerätekontexts ab.                                                                                                 |
| [**Getobject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Ruft Informationen für das angegebene Grafikobjekt ab.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Ruft den Typ des angegebenen Objekts ab.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Ruft ein Handle für einen der Stockstifte, Pinsel, Schriftarten oder Paletten ab.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Gibt einen Gerätekontext frei und gibt ihn für die Verwendung durch andere Anwendungen frei.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Aktualisiert den angegebenen Drucker- oder Plottergerätekontext unter Verwendung der angegebenen Informationen.                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Stellt den angegebenen Zustand eines Gerätekontexts wieder her.                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Speichert den aktuellen Zustand des angegebenen Gerätekontexts, indem Daten, die ausgewählte Objekte und Grafikmodi beschreiben, in einen Kontextstapel kopiert werden. |
| [**Auswählenobjekt**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Wählt ein Objekt im angegebenen Gerätekontext aus.                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Legt die aktuelle Pinselfarbe des Gerätekontexts auf den angegebenen Farbwert fest.                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Legt die aktuelle Stiftfarbe des Gerätekontexts auf den angegebenen Farbwert fest.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Legt das Layout für einen Gerätekontext fest.                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Gibt ein Handle für das Fenster zurück, das einem Gerätekontext zugeordnet ist.                                                                          |



 

 

 
