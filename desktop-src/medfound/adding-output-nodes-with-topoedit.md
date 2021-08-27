---
description: Hinzufügen von Ausgabeknoten mit TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Hinzufügen von Ausgabeknoten mit TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e975e332a464218f8629363f34a2d3fbef0e5a49
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481976"
---
# <a name="adding-output-nodes-with-topoedit"></a>Hinzufügen von Ausgabeknoten mit TopoEdit

In einer Topologie stellt ein Ausgabeknoten eine Mediensenke dar, die Mediendaten von einem Transformationsknoten empfängt und zur Wiedergabe darstellt. Der Typ des Ausgabeknotens hängt vom Medientyp des Quellknotens ab.

Die folgende Tabelle zeigt den Menü-/Symbolleistenbefehl zum Hinzufügen eines Ausgabeknotens zur Topologie.




| Quellmedientyp | Menü-/Symbolleistenbefehl | BESCHREIBUNG | 
|-------------------|----------------------|-------------|
| Audiodatenstrom | Klicken Sie <strong>im Menü Topologie</strong> auf SAR <strong>hinzufügen.</strong> | Erstellt einen Ausgabeknoten für den Streaming Audio Renderer (SAR), der einen Audiodatenstrom über ein Audiogerät wie eine Soundkarte abspielt. | 
| Videostream | Klicken Sie <strong>im Menü Topologie</strong> auf <strong>EVR hinzufügen.</strong> | Erstellt einen Ausgabeknoten für den erweiterten Videorenderer (EVR), der Frames für einen Videostream anzeigt. | 
| Benutzerdefinierte Mediensenke | <ol><li>Klicken Sie <strong>im Menü Topologie</strong> auf <strong>Benutzerdefinierte Senke hinzufügen.</strong><br /> Das <strong>Dialogfeld Benutzerdefinierte GUID eingeben</strong> wird geöffnet.<br /></li><li><p>Geben Sie <strong>im Feld GUID:</strong> die GUID Ihrer benutzerdefinierten Senke ein, die Sie der Topologie hinzufügen möchten.<br /></p><blockquote>[!Note]<br />TopoEdit erwartet die GUID im Format "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}". Andernfalls kann der Knoten nicht hinzugefügt werden, und es wird die Fehlermeldung "Ungültige GUID" angezeigt.</blockquote><p><br /></p></li><li>Klicken Sie auf <strong>OK</strong>.<br /></li></ol> | Erstellt einen Ausgabeknoten für die Streamsenke für eine benutzerdefinierte Medienquelle.<br /> Die benutzerdefinierte Senke muss <strong>CoCreateInstance unterstützen,</strong> damit die Senke mit einer CLSID angegeben werden kann.<br /> | 




 

TopoEdit erstellt den angegebenen Ausgabeknoten. Im **Topologiebereich wird** der Ausgabeknoten als grünes Feld mit dem Namen der Streamsenke angezeigt.

Informationen zum programmgesteuerten Hinzufügen von Ausgabeknoten mithilfe Media Foundation-APIs finden Sie unter [Erstellen von Ausgabeknoten.](creating-output-nodes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Topologien mit TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




