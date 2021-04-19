---
title: Implementieren In-Place Aktivierung
description: Implementieren In-Place Aktivierung
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337579"
---
# <a name="implementing-in-place-activation"></a>Implementieren In-Place Aktivierung

Die direkte Aktivierung ermöglicht einem Benutzer die Interaktion mit einem eingebetteten Objekt, ohne das Container Dokument zu überlassen. Wenn ein Benutzer das Objekt aktiviert, ersetzt eine zusammen *gesetzte Menüleiste* , die Elemente aus den Menüleisten der Containeranwendung und der Serveranwendung enthält, die Hauptmenüleiste des Containers. Die Befehle und Features beider Anwendungen stehen dem Benutzer zur Verfügung, einschließlich kontextbezogener Hilfe für das aktive Objekt. Wenn ein Benutzer mit der Arbeit mit einem nicht-Objekt Teil des Dokuments beginnt, wird das Objekt deaktiviert, sodass das ursprüngliche Menü des Container Dokuments das zusammengesetzte Menü ersetzt.

Diese Funktion wurde ursprünglich durch den Namen der direkten *Bearbeitung geführt*. Der Name wurde geändert, da die Bearbeitung nur eine Möglichkeit für einen Benutzer ist, mit einem laufenden Objekt zu interagieren. Sound Clips können z. b. durch ein-und nicht bearbeitet werden. Video Clips können anstelle der Bearbeitung angezeigt werden. Die direkte Aktivierung ist im Fall von Videoclips besonders passend, da Sie Sie direkt ausführen können, ohne ein separates Fenster aufzurufenden zu müssen. Dies kann wichtig sein, wenn das Video in Verbindung mit angrenzenden Textdaten im Container Dokument angezeigt werden soll.

Die Implementierung der direkten Aktivierung ist für Container-und Server Anwendungen streng optional. OLE unterstützt weiterhin das Modell, in dem das Aktivieren eines Objekts bewirkt, dass die Serveranwendung ein separates Fenster öffnet. Verknüpfte Objekte werden immer in einem separaten Fenster geöffnet, um hervorzuheben, dass Sie sich in einem separaten Dokument befinden.

Die direkte Aktivierung beginnt mit dem-Objekt als Reaktion auf einen [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) -Aufrufe aus dem Container. Dieser Vorgang erfolgt in der Regel als Reaktion darauf, dass ein Benutzer auf das Objekt doppelklickt oder im Menü Bearbeiten der Containeranwendung einen Befehl (Verb) auswählt.

Das direkte Fenster empfängt Tastatur-und Maus Eingaben, während das eingebettete Objekt aktiv ist. Wenn ein Benutzer Befehle in der zusammengesetzten Menüleiste auswählt, werden der Befehl und die zugehörigen Menü Meldungen an den Container oder die Objekt Anwendung gesendet, je nachdem, welcher Besitzer das jeweilige Dropdown Menü besitzt. Eingaben über die Lineale, Symbolleisten oder Frame Zusatzelemente eines Objekts gelangen direkt zum eingebetteten Objekt, das diese Fenster besitzt.

Ein direkt aktiviertes eingebettetes Objekt bleibt aktiv, bis entweder der Container es als Antwort auf die Benutzereingabe deaktiviert hat oder das Objekt freiwillig den aktiven Zustand erhält, wie es beispielsweise bei einem Videoclip der Fall ist. Ein Benutzer kann ein Objekt deaktivieren, indem er in das Container Dokument, aber außerhalb des direkt aktivierten Fensters des Objekts klickt oder einfach durch Klicken auf ein anderes Objekt. Ein direkt aktiviertes Objekt bleibt aktiv, wenn der Benutzer jedoch auf die Titelleiste des Containers, die Scrollleiste oder auf die Menüleiste klickt.

Sie können einen Server mit direkten Aktivierungs Objekten entweder als Prozess interner Server (dll) oder als lokaler Server (exe) implementieren. In beiden Fällen enthält die zusammengesetzte Menüleiste Elemente (normalerweise Dropdown Menüs) aus den Server-und Container Prozessen. Im Fall eines in-Process-Servers ist das direkte Aktivierungsfenster einfach ein weiteres untergeordnetes Fenster in der Fenster Hierarchie des Containers, das seine Eingabe über das nachrichtenpump der Containeranwendung empfängt.

Im Fall eines lokalen Servers gehört das direkte Aktivierungsfenster zum Server Anwendungsprozess des eingebetteten Objekts, aber das übergeordnete Fenster gehört zum Container. Die Eingabe für das Fenster direkt Aktivierung wird in der Nachrichten Warteschlange des Servers angezeigt und von der Nachrichten Schleife des Servers gesendet. Die OLE-Bibliotheken sind dafür verantwortlich zu sehen, dass Menübefehle und Meldungen ordnungsgemäß weitergeleitet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 




