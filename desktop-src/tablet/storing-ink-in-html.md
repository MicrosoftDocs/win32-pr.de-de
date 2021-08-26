---
description: Es ist in der Regel wünschenswert, einen komplizierteren Satz von Informationen zu kopieren, als im ink serialisierten Format (ISF) enthalten sein kann.
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Speichern von Ink in HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d8949582c5743ba7be5ac664627792c7b7f8a0cd5968a67f5db08b6428cb886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934360"
---
# <a name="storing-ink-in-html"></a>Speichern von Ink in HTML

Es ist in der Regel wünschenswert, einen komplizierteren Satz von Informationen zu kopieren, als im ink serialisierten Format (ISF) enthalten sein kann. HTML ist aufgrund seiner starken Akzeptanz als Branchenstandard und seiner Fähigkeit, heterogene Inhalte darzustellen, besonders nützlich als Interoperabilitätsformat.

HTML ist für viele Entwickler allgemein verständlich, gut dokumentiert und vertraut. Es gibt viele Tools für die HTML-Produktion. Darüber hinaus enthält Microsoft Windows APIs (Application Programming Interfaces) zum Rendern und Bearbeiten von HTML. Schließlich stellen die Tablet PC Platform-APIs das persistente GIF-Persistenzformat bereit, das für die Einbettung in andere Formate geeignet ist, vor allem HTML. Dieses Format besteht aus einer GIF-Datei mit serialisiertes Freihandformat (ISF), die in einen Anwendungserweiterungsblock eingebettet ist.

Diese GIF-Dateien sind Darstellungen von Freihandobjekten, die:

-   Rendern in Nicht-Ink-fähigen Anwendungen, z. B. Browsern oder Legacy-Textprozessoren.
-   Enthält alle erforderlichen Informationen aus der ursprünglichen Ink, die zu Bearbeitungs- oder Erkennungszwecken verwaltet werden sollen.

Diese GIF-Dateien können mithilfe der Persistenzmethoden der Tablet PC Platform-APIs erstellt werden. Es handelt sich um GIFs, die die GIF-Erweiterung verwenden sollten. Für eine Anwendung, die nicht ink-fähig ist, gibt es nichts anderes als ein normales GIF. Für eine Anwendung mit Ink-Aktivierung gibt es jedoch einen umfangreichen Satz von Daten, die dem Image zugrunde liegen.

Nachdem sie von den Tablet PC Platform-APIs erstellt wurde, wird auf ein verstärktes GIF durch ein IMG-Tag in HTML verwiesen. Der HTML-Code wird dann im STANDARDMÄßIGEN CF \_ HTML-Zwischenablageslot gespeichert. Dadurch kann der HTML-Code für andere Anwendungen sichtbar sein, unabhängig davon, ob sie ink-fähig sind. Das Image selbst kann im Windows Internetcache gespeichert und nach einer angemessenen Zeitspanne auf das Altern festgelegt werden.

Bestimmte Adornments für das IMG-Tag werden bereitgestellt oder sind erforderlich. Diese Adornments identifizieren den HTML-Code als mit Ink. Im folgenden Beispiel wird mithilfe von HTML-Tags auf ein verstärktes GIF verwiesen:

`<img href="34372423432.gif" />`

Wenn auf das Bild auf andere Weise verwiesen werden muss, z. B. mit cascading stylesheets oder Vector Markup Language (VML), sollte weiterhin ein IMG-Tag vorhanden sein, das auf das Image verweist. Dies ermöglicht das Ausschneiden und Einfügen in und aus jeder Anwendung, die HTML-Darstellungen von Ink akzeptiert.

Anwendungen, die Freihand in HTML unterstützen, sollten:

-   Generieren Sie \_ CF-HTML, wenn der Benutzer eine Kopie ausführt. Verwenden Sie beim Generieren von CF \_ HTML beim Kopieren (oder Speichern als HTML) die [Microsoft.Ink.Ink.Save-Methode,](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) und geben Sie den [Wert Microsoft.Ink.PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) im *p-Parameter* an, um ein verstärktes GIF-Bild zu generieren. Der alte Text sollte auf das genaueste Erkennungsergebnis festgelegt werden. Sie können die Positionierung nach Bedarf entweder auf absolut oder an Ort und Stelle festlegen.
-   Überprüfen Sie alle IMG-Tags, um zu ermitteln, ob Bilder, auf die sie zeigen, Ink enthalten, ob der \_ CF-HTML-Slot für ein Einfügen ausgewählt wird. Wenn ja, behandeln Sie die Bilder intern als [Ink-Objekte.](/previous-versions/aa515768(v=msdn.10)) Obwohl in dieser Version nur GIF-Dateien unterstützt werden, sollte Ihre Anwendung auch Nicht-GIF-Bilder überprüfen, falls in Zukunft zusätzliche Bildformate unterstützt werden.
-   Unterstützt das Kopieren und Einfügen von ISF. Anwendungen, die HTML unterstützen, sollten auch ISF unterstützen, um die Interoperabilität mit Ink-fähigen Anwendungen zu verbessern, die HTML nicht erkennen. Dies ähnelt der Konvention, dass Anwendungen, die HTML in der Zwischenablage platzieren, auch Text platzieren.

Weitere Informationen zu verstärkten GIFs finden Sie unter [Bausteine.](building-blocks.md)

 

 
