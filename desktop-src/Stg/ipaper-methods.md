---
title: IPaper-Methoden
description: Stellt COPaper-Objekte bereit, die hauptsächlich über ihre native IPaper-Schnittstelle gesteuert werden.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- Ipaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a45322e35f07a6f136e76ecaad6ae237891a741dfb44a6b5db0702c87bda33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662720"
---
# <a name="ipaper-methods"></a>IPaper-Methoden

**StoServe stellt** COPaper-Objekte bereit, die hauptsächlich über ihre native **IPaper-Schnittstelle gesteuert** werden.

In der folgenden Tabelle sind **die IPaper-Methoden** von IPAPER aufgeführt. H im verzeichnis der \\ gleichgeordneten INC.



| Methode    | Beschreibung                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Initialisiert das Papierobjekt und erstellt ein Ink-Datenarray.                 |
| Sperre      | Ermöglicht die Clientsteuerung des Papiers und sperrt andere Clients.      |
| Unlock    | Gibt die Clientsteuerung des Papiers auf.                           |
| Laden      | Lädt Papierinhalte aus der Verbunddatei des Clients und benachrichtigt Senken. |
| Speichern      | Speichert Papierinhalte in der Verbunddatei des Clients.                      |
| InkStart  | Startet die Farbzeichnung auf der Papieroberfläche.                      |
| InkDraw   | Legt Ink-Datenpunkte auf der elektronischen Papieroberfläche ab.               |
| InkStop   | Beendet das Zeichnen von Ink-Zeichen auf der Papieroberfläche.                             |
| Löschen     | Löscht den aktuellen Papierinhalt und benachrichtigt Senken.                 |
| Größe ändern    | Passt die Größe des Zeichnungsdokumentrechtecks an und benachrichtigt Senken.        |
| Zeichnen    | Der Inhalt des Papierobjekts wird neu gedrammt, und senken werden benachrichtigt.                |



 

Die für dieses Codebeispiel für Verbunddateien von Interesse sind [**Load**](ipaper--load.md), [**Save**](ipaper--save.md)und [**Redraw.**](ipaper--redraw.md)

[**InkStart,**](inkstart-method.md) [**InkDraw**](inkdraw-method.md)und [**InkStop**](cguipaper-methods.md) sind Methoden, die von Clients verwendet werden, um COPaper zum Aufzeichnen von Freischaltsequenzen zu befehlen. Der Client antwortet in der Regel auf eine WM-LBUTTONDOWN-Nachricht als Start einer Ink-Zeichnungssequenz, indem er \_ **InkStart** auf COPaper aufruft. Wenn der Benutzer die Maus oder den Stift bewegt, um zu zeichnen, während er die linke Schaltfläche gedrückt hält, antwortet der Client mit entsprechenden Aufrufen von InkDraw auf wiederholte WM \_ MOUSEMOVE-Nachrichten.  Wenn der Benutzer die linke Maustaste loslässt, antwortet der Client auf eine WM-LBUTTONUP-Nachricht mit einem Aufruf von \_ **InkStop,** der das Ende der Freitext-Zeichnungssequenz markiert.

[**InkStart teilt**](inkstart-method.md) COPaper die Startposition für die Zeichnungssequenz in Clientfensterkoordinaten mit. Außerdem wird die aktuell ausgewählte Farbe und Breite der Ink-Farbe übergibt. Der Client behält diese Auswahl bei. COPaper zeichnet sie lediglich auf, wenn der **InkStart-Aufruf** erfolgt. [**InkDraw**](inkdraw-method.md) wird wiederholt aufgerufen, um COPaper die Folge von Fensterkoordinaten zu mitteilen, die die Zeichnungsbewegung der Maus oder des Stifts darstellen. [**InkStop weist**](cguipaper-methods.md) COPaper an, das Ende einer Zeichnungssequenz zu markieren.

 

 




