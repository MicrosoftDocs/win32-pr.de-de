---
title: CGuiPaper-Methoden
description: Die Methoden von CGuiPaper werden wie folgt zusammengefasst. Diese Methoden werden alle in GUIPAPER implementiert. Cpp.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78f6d6fa04bba96d8cfb9e7ac23708560221f23b98437fa33f21245d28daf60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962477"
---
# <a name="cguipaper-methods"></a>CGuiPaper-Methoden

Die Methoden von CGuiPaper werden wie folgt zusammengefasst. Diese Methoden werden alle in GUIPAPER implementiert. Cpp.



| Methode                                                         | Beschreibung                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL Init(HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Initialisiert den GuiPaper. Fordert den Server auf, ein COPaper-Objekt zu erstellen.                                                     |
| HRESULT DrawOn(void);                                          | Sperrt Papier zum ausschließlichen Zeichnen durch diesen Client.                                                                   |
| HRESULT DrawOff(void);                                         | Entsperrt Papier, damit andere Clients zeichnen können.                                                                         |
| HRESULT ClearWin(void);                                        | Löschen des Anzeigefensters, behält jedoch Freik-Daten bei.                                                                           |
| HRESULT PaintWin(void);                                        | Clears window and repaints with current ink data (Fenster löschen und mit aktuellen Freik-Daten neu gepaint).                                                                     |
| HRESULT Erase(void);                                           | Löscht den aktuellen Zeichnungsinhalt und löscht das Anzeigefenster.                                                             |
| HRESULT Resize(WORD wWidth, WORD wHeight);                     | Die Größe des Anzeigefensters wird geändert.                                                                                           |
| HRESULT InkWidth(SHORT nInkWidth);                             | Legt die aktuelle Breite von Ink für das Zeichnen fest.                                                                                   |
| HRESULT InkColor(COLORREF crInkColor);                         | Legt die aktuelle Ink-Farbe für das Zeichnen fest.                                                                                   |
| HRESULT InkSaving(BOOL bInkSaving);                            | Aktiviert und deaktiviert das Speichern von Ink-Daten in COPaper.                                                                          |
| HRESULT InkStart(SHORT nX, SHORT nY);                          | Startet die Zeichensequenz für Ink.                                                                                          |
| HRESULT InkDraw(SHORT nX, SHORT nY);                           | Zeichnet Ink-Sequenzdaten.                                                                                              |
| HRESULT InkStop(SHORT nX, SHORT nY);                           | Beendet die Zeichensequenz für Ink-Zeichen.                                                                                           |
| HRESULT ConnectPaperSink(void);                                | Verbindet das PaperSink-Clientobjekt mit der COPaper-Quelle des Servers.                                                    |
| HRESULT DisconnectPaperSink(void);                             | Trennen Sie das PaperSink-Clientobjekt von der COPaper-Quelle des Servers.                                                |
| HRESULT Load(void);                                            | Lädt Ink-Daten aus der aktuellen Verbunddatei.                                                                            |
| HRESULT Save(void);                                            | Speichert vorhandene Ink-Daten in der aktuellen Verbunddatei.                                                                     |
| HRESULT AskSave(void);                                         | Überprüft, ob das Zeichnen geändert wurde. Wenn ja, wird das Dialogfeld angezeigt, in dem der Benutzer gefragt wird, ob Änderungen zu speichern sind, und reagiert entsprechend. |
| HRESULT Open(void);                                            | Zeigt das allgemeine Win32-Dialogfeld an. Öffnet die vorhandene Verbunddatei für Papierdaten.                                               |
| HRESULT SaveAs(void);                                          | Zeigt das allgemeine Win32-Dialogfeld an. Speichert aktuelle Papierdaten in einer umbenannten Datei.                                              |
| COLORREF PickColor(void);                                      | Zeigt das Win32-Ommon-Dialogfeld an. Fordert den Benutzer auf, eine neue Stiftfarbe zu wählen.                                                      |



 

Die **Init-Methode** erstellt das serverbasierte COPaper-Objekt und weist den \_ pIPaper-Member von CGuiPaper zu.

Die **Methoden AskSave,** **Open,** **SaveAs** und **PickColor** bieten vertrautes GUI-Verhalten mithilfe gängiger Win32-Dialogfelder. Beispielsweise verwendet die **Open-Methode** das Dialogfeld Win32 Open File Name (Win32-Dateinamen öffnen), um den Benutzer auf zu bitten, einen Dateinamen zum Öffnen anzugeben.

Die **Load-** **und Save-Methoden** werden später in dieser Tour ausführlich behandelt.

**InkSaving,** **InkStart,** **InkDraw** und **InkStop** sind die zentralen Methoden für die Zeichnungsfunktionalität der **StoClien-Anwendung.** **StoClien verwendet** diese CGuiPaper-Methoden, um die interaktiven Zeichnungsdaten zu erfassen, anzuzeigen und zu speichern, während sie unter Benutzersteuerung auftreten. Sie zeichnen das gezeichnete Bild in das Clientfenster und übergeben die Zeichnungsdaten an COPaper auf dem Server. COPaper übersetzt die Zeichnungsdaten in Ink-Datenpakete für die Speicherung.

 

 




