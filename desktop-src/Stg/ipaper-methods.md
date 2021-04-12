---
title: IPaper-Methoden
description: Stellt copaper-Objekte bereit, die hauptsächlich von ihrer nativen iPaper-Schnittstelle gesteuert werden.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207301"
---
# <a name="ipaper-methods"></a>IPaper-Methoden

**Stoservice** bietet copaper-Objekte, die in erster Linie von ihrer nativen **iPaper** -Schnittstelle gesteuert werden.

In der folgenden Tabelle sind die **iPaper** -Methoden aus iPaper aufgeführt. H im neben geordneten \\ Inc-Verzeichnis.



| Methode    | BESCHREIBUNG                                                         |
|-----------|---------------------------------------------------------------------|
| Initpaper | Initialisiert ein Papierobjekt und erstellt ein frei Hand Daten Array.                 |
| Sperre      | Ermöglicht die Client Steuerung des Papiers und sperrt andere Clients.      |
| Unlock    | Gibt die Client Steuerung des Papiers aus.                           |
| Laden      | Lädt Papier Inhalt aus der Verbund Datei des Clients und benachrichtigt senken. |
| Speichern      | Speichert Papier Inhalt in der Verbund Datei des Clients.                      |
| Inkstart  | Startet das Zeichnen von Farb Freihand auf der Papieroberfläche.                      |
| Inkdraw   | Legt frei Hand Datenpunkte auf der elektronischen Papieroberfläche ab.               |
| Inkstopps   | Stoppt das Zeichnen von frei Hand Eingaben auf die Papieroberfläche.                             |
| Löschen     | Löscht den aktuellen Papier Inhalt und benachrichtigt senken.                 |
| Größe ändern    | Ändert die Größe der Größe des Zeichnungs Papier Rechtecks und benachrichtigt senken.        |
| Neu zeichnen    | Zeichnet den Inhalt des Papier Objekts neu und benachrichtigt senken.                |



 

Relevante Methoden für dieses Codebeispiel für Verbund Dateien sind [**Laden**](ipaper--load.md), [**Speichern**](ipaper--save.md)und [**neu zeichnen**](ipaper--redraw.md).

[**Inkstart**](inkstart-method.md), [**inkdraw**](inkdraw-method.md)und [**inkstopps**](cguipaper-methods.md) sind Methoden, die von Clients verwendet werden, um copaper zum Aufzeichnen von Handzeichen Sequenzen zu Befehlen. Der Client antwortet in der Regel auf eine WM- \_ lbuttondown-Meldung als Anfang einer frei Hand Zeichnungs Sequenz durch Aufrufen von **inkstart** bei copaper. Wenn der Benutzer die Maus oder den Stift zum Zeichnen bewegt, während er die linke Schaltfläche gedrückt hält, antwortet der Client auf wiederholte WM- \_ MouseMove-Meldungen mit entsprechenden Aufrufen von **inkdraw**. Wenn der Benutzer die linke Maustaste loslässt, antwortet der Client auf eine WM- \_ lbuttonup-Meldung mit dem aufzurufenden Ink-Befehl, der das Ende der frei Hand Zeichnungs Sequenz markiert. 

[**Inkstart**](inkstart-method.md) weist copaper die Anfangsposition der Zeichnungs Sequenz in Client Fenster Koordinaten zu. Außerdem übergibt Sie die aktuell ausgewählte frei Hand Farbe und-Breite. Diese Auswahl wird vom Client beibehalten. Copaper zeichnet Sie nur auf, wenn der **inkstart** -Rückruf erfolgt. [**Inkdraw**](inkdraw-method.md) wird wiederholt aufgerufen, um copaper die Abfolge der Fenster Koordinaten anzugeben, die die Zeichnungs Bewegung der Maus oder des Stifts darstellen. [**Inkbeenden**](cguipaper-methods.md) weist copaper an, das Ende einer Zeichnungs Sequenz zu markieren.

 

 




