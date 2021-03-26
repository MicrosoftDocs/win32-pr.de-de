---
description: Die folgenden Funktionen werden mit Geräte Kontexten verwendet.
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: Gerätekontext Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 625b81b999526d84af4b58f2dddbc280643bcd35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754457"
---
# <a name="device-context-functions"></a>Gerätekontext Funktionen

Die folgenden Funktionen werden mit Geräte Kontexten verwendet.



| Funktion                                                   | BESCHREIBUNG                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canceldc**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | Bricht jeden ausstehenden Vorgang für den angegebenen Gerätekontext ab.                                                                            |
| [**Changedisplaysettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | Ändert die Einstellungen für das Standard Anzeigegerät in den angegebenen Grafikmodus.                                                        |
| [**Changedisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | Ändert die Einstellungen des angegebenen Anzeige Geräts in den angegebenen Grafikmodus.                                                      |
| [**"Kreatecompatibledc"**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | Erstellt einen Arbeitsspeicher-Gerätekontext, der mit dem angegebenen Gerät kompatibel ist.                                                                     |
| [**-**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | Erstellt einen Gerätekontext für ein Gerät mit dem angegebenen Namen.                                                                           |
| [**Nicht formatiert**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | Erstellt einen Informations Kontext für das angegebene Gerät.                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | Löscht den angegebenen Gerätekontext.                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | Löscht einen logischen Stift, Pinsel, eine Schriftart, eine Bitmap, eine Region oder eine Palette und gibt dabei alle Systemressourcen frei, die dem-Objekt zugeordnet sind.                  |
| [**Gerätefunktionen**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | Ruft die Funktionen eines Druckergerätetreibers ab.                                                                                    |
| [**Drawescape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | Bietet Zeichnungsfunktionen der angegebenen Videoanzeige, die nicht direkt über die Grafikgeräte Schnittstelle verfügbar sind.       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | Ruft Informationen über die Anzeigegeräte in einem System ab.                                                                              |
| [**Enumdisplaysettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | Ruft Informationen zu einem der Grafikmodi für ein Anzeigegerät ab.                                                               |
| [**Enumdisplaysettingsex**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | Ruft Informationen zu einem der Grafikmodi für ein Anzeigegerät ab.                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | Listet die Stifte oder Pinsel auf, die für den angegebenen Gerätekontext verfügbar sind.                                                                |
| [**"Umumubjectsproc"**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | Eine Anwendungs definierte Rückruffunktion, die mit der [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion verwendet wird.                                       |
| [**Getcurrentobject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | Ruft ein Handle für ein Objekt vom angegebenen Typ ab, das im angegebenen Gerätekontext ausgewählt wurde.                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | Ruft ein Handle für einen Anzeigegeräte Kontext für den Client Bereich eines angegebenen Fensters oder für den gesamten Bildschirm ab.                        |
| [**Getdcbrushcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | Ruft die aktuelle Pinsel Farbe für den angegebenen Gerätekontext ab.                                                                       |
| [**Getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | Ruft ein Handle für einen Anzeigegeräte Kontext für den Client Bereich eines angegebenen Fensters oder für den gesamten Bildschirm ab.                        |
| [**Getdcorgex**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | Ruft den endgültigen Übersetzungs Ursprung für einen angegebenen Gerätekontext ab.                                                                    |
| [**Getdcpcolor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | Ruft die aktuelle Stift Farbe für den angegebenen Gerätekontext ab.                                                                         |
| [**Getde vicecaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | Ruft gerätespezifische Informationen für das angegebene Gerät ab.                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | Ruft das Layout eines Geräte Kontexts ab.                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | Ruft Informationen für das angegebene Grafik Objekt ab.                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | Ruft den Typ des angegebenen Objekts ab.                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | Ruft ein Handle für einen der Stock Stifte, Pinsel, Schriftarten oder Paletten ab.                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | Gibt einen Gerätekontext frei und gibt ihn für die Verwendung durch andere Anwendungen frei.                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | Aktualisiert den angegebenen Drucker-oder plotgerätekontext unter Verwendung der angegebenen Informationen.                                                  |
| [**Restoredc**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | Stellt einen Gerätekontext in den angegebenen Zustand wieder her.                                                                                         |
| [**Savedc**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | Speichert den aktuellen Zustand des angegebenen Geräte Kontexts, indem Daten, die ausgewählte Objekte und Grafikmodi beschreiben, in einen Kontext Stapel kopiert werden. |
| [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | Wählt ein Objekt in den angegebenen Gerätekontext aus.                                                                                      |
| [**Setdcbrushcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Legt die aktuelle Pinsel Farbe des Geräte Kontexts auf den angegebenen Farbwert fest.                                                                 |
| [**Setdcpcolor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | Legt die aktuelle Stift Farbe des Geräte Kontexts auf den angegebenen Farbwert fest.                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | Legt das Layout für einen Gerätekontext fest.                                                                                                     |
| [**Windowfromdc**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | Gibt ein Handle für das Fenster zurück, das einem Gerätekontext zugeordnet ist.                                                                          |



 

 

 
