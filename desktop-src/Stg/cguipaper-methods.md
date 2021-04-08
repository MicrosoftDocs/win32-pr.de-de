---
title: Cguipaper-Methoden
description: Die Methoden von cguipaper werden wie folgt zusammengefasst. Diese Methoden werden alle in guipaper implementiert. CPP.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708207"
---
# <a name="cguipaper-methods"></a>Cguipaper-Methoden

Die Methoden von cguipaper werden wie folgt zusammengefasst. Diese Methoden werden alle in guipaper implementiert. CPP.



| Methode                                                         | BESCHREIBUNG                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Bool init (HINSTANCE hInst, HWND hWnd, Tchar \* pszcmdlinefile); | Initialisiert das guipaper. Fordert den Server auf, ein copaper-Objekt zu erstellen.                                                     |
| HRESULT DrawOn (void);                                          | Sperrt das Papier, das exklusiv von diesem Client gezeichnet wird.                                                                   |
| HRESULT drawoff (void);                                         | Entsperrt das Papier, damit andere Clients zeichnen können.                                                                         |
| HRESULT clearwin (void);                                        | Löscht das Anzeige Fenster, behält jedoch frei Hand Daten bei.                                                                           |
| HRESULT-malzwilling (void);                                        | Löscht Fenster und zeichnet mit aktuellen frei Hand Daten.                                                                     |
| HRESULT-Löschung (void);                                           | Löscht den aktuellen Zeichnungs Inhalt und löscht das Anzeige Fenster.                                                             |
| HRESULT Resize (Wort wwidth, Wort Wheight);                     | Ändert die Größe des Anzeige Fensters.                                                                                           |
| HRESULT inkwidth (kurzninkwidth);                             | Legt die aktuelle Handschrift Breite für das Zeichnen fest.                                                                                   |
| HRESULT inkcolor (COLORREF crinkcolor);                         | Legt die aktuelle frei Hand Farbe zum Zeichnen fest.                                                                                   |
| HRESULT inksave (bool binksave);                            | Schaltet die frei Hand Datenspeicherung in copaper ein und aus.                                                                          |
| HRESULT inkstart (kurzes NX, kurzes NY);                          | Startet die frei Hand Zeichnungs Sequenz.                                                                                          |
| HRESULT inkdraw (kurzes NX, kurzes NY);                           | Zeichnet frei Hand Sequenzdaten.                                                                                              |
| HRESULT inkstoppt (kurzes NX, kurzes NY);                           | Beendet die frei Hand Zeichnungs Sequenz.                                                                                           |
| HRESULT connecttaschen Sink (void);                                | Stellt eine Verbindung zwischen dem Client-Taschen Senk Objekt und der Server-copaper-Quelle her                                                    |
| HRESULT disconnecttaschen Sink (void);                             | Trennen Sie die Verbindung zwischen dem Client-Taschen Senk Objekt und der Server Kopier Quelle.                                                |
| HRESULT-Auslastung (void);                                            | Lädt frei Hand Daten aus der aktuellen Verbund Datei.                                                                            |
| HRESULT speichern (void);                                            | Speichert vorhandene frei Hand Daten in der aktuellen Verbund Datei.                                                                     |
| HRESULT asksave (void);                                         | Überprüft, ob das Zeichnen geändert wurde. Wenn dies der Fall ist, wird ein Dialogfeld angezeigt, in dem der Benutzer gefragt wird, ob Änderungen gespeichert und |
| HRESULT geöffnet (void);                                            | Zeigt das allgemeine Win32-Dialogfeld an. Öffnet eine vorhandene Papier Daten-Verbund Datei.                                               |
| HRESULT SaveAs (void);                                          | Zeigt das allgemeine Win32-Dialogfeld an. Speichert die aktuellen Papier Daten in der umbenannten Datei.                                              |
| COLORREF pickcolor (void);                                      | Zeigt das Win32 gebräuchliche-Dialogfeld an. Fordert den Benutzer auf, neue Stift Farbe auszuwählen.                                                      |



 

Die **Init** -Methode erstellt das serverbasierte copaper-Objekt und weist das m pipaper-Element von cguipaper zu \_ .

Die Methoden **asksave**, **Open**, **SaveAs** und **pickcolor** stellen ein bekanntes GUI-Verhalten mithilfe von Win32-gängigen Dialogfeldern bereit. Die Methode **Open** verwendet beispielsweise das Dialogfeld Win32 Open File Name, um den Benutzer zur Angabe eines Datei namens zum Öffnen aufzufordern.

Die **Load** -und **Save** -Methoden werden später in dieser Tour ausführlich behandelt.

**Inksave**, **inkstart**, **inkdraw** und **inkend** sind die zentralen Methoden für die Zeichnungsfunktionen der **stoclien** -Anwendung. **Stoclien** verwendet diese cguipaper-Methoden, um die interaktiven Zeichnungsdaten zu erfassen, anzuzeigen und zu speichern, während Sie unter Benutzer Steuerelement auftreten. Sie führen eine duale Rolle aus, um das gezeichnete Bild im Client Fenster zu zeichnen und die Zeichnungsdaten auf dem Server an copaper zu übergeben. Copaper übersetzt die Zeichnungsdaten zum Speichern in frei Hand Datenpakete.

 

 




