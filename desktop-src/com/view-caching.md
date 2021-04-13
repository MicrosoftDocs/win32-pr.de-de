---
title: Zwischenspeichern anzeigen
description: Zwischenspeichern anzeigen
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c5bc2555e907cdc4e600465b807387c3a5548
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391048"
---
# <a name="view-caching"></a>Zwischenspeichern anzeigen

Eine Containeranwendung muss in der Lage sein, eine Darstellung eines Objekts zu erhalten, um Sie für Benutzer anzuzeigen oder zu drucken, wenn das Dokument geöffnet ist, die Serveranwendung des Objekts jedoch nicht ausgeführt wird oder nicht auf dem Computer des Benutzers installiert ist. Es wird jedoch davon ausgegangen, dass die Server für alle Objekte, die möglicherweise in einem Dokument gefunden werden, auf dem Computer jedes Benutzers installiert sind und immer Bedarfs gesteuert ausgeführt werden können. Der Standard Objekt Handler, der jederzeit verfügbar ist, löst dieses Problem durch Zwischenspeichern von Objekt Präsentationen im Speicher des Dokuments und Bearbeiten dieser Präsentationen auf allen Plattformen, unabhängig von der Verfügbarkeit des Objekt Servers auf einer bestimmten Installation des Containers.

Container können Zeichnungs Präsentationen für ein oder mehrere bestimmte Zielgeräte verwalten, zusätzlich zu dem, das für die Verwaltung des Objekts auf dem Bildschirm erforderlich ist. Wenn Sie das Objekt von einer Plattform zu einem anderen portieren, werden die Datenformate des Objekts von OLE automatisch in diejenigen konvertiert, die auf der neuen Plattform unterstützt werden. Wenn Sie z. b. ein Objekt von Windows in den Macintosh-Code verschieben, konvertiert OLE seine metadateipräsentationen in PICT-Formate.

Um dem Benutzer eine exakte Darstellung eines eingebetteten Objekts zu präsentieren, initiiert die Containeranwendung des Objekts einen Dialog mit dem Objekt Handler, der Daten und Zeichen Anweisungen anfordert. Der Handler muss die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)-, [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)-und [**iolecache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) -Schnittstellen implementieren, um die Anforderungen des Containers erfüllen zu können.

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ermöglicht es einer OLE-Containeranwendung, Daten aus den eingebetteten oder verknüpften Objekten zu erhalten und Daten zu senden. Wenn sich Daten in einem Objekt ändern, bietet diese Schnittstelle eine Möglichkeit für das Objekt, die neuen Daten für den Container verfügbar zu machen, und stellt dem Container eine Möglichkeit zum Aktualisieren der Daten in der zugehörigen Kopie des Objekts bereit. (Eine Erörterung der Datenübertragung im Allgemeinen finden Sie in Kapitel 4, Datenübertragung.)

Die [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) -Schnittstelle ähnelt der [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle, mit der Ausnahme, dass Sie ein Objekt anfordert, sich selbst in einem Gerätekontext zu zeichnen, z. b. einem Bildschirm, einem Drucker oder einer Metadatei, anstatt die Daten in den Arbeitsspeicher oder ein anderes Übertragungsmedium zu verschieben Der Zweck der-Schnittstelle besteht darin, einen OLE-Container zu aktivieren, um alternative bildliche Darstellungen der eingebetteten Objekte zu erhalten, deren Daten bereits vorhanden sind. auf diese Weise wird der Aufwand vermieden, bei dem eine vollständige Übertragung völlig neuer Instanzen derselben Datenobjekte erforderlich ist, um neue Zeichnungs Anweisungen zu erhalten. Stattdessen ermöglicht die **IViewObject2**-Schnittstelle dem Container, ein Objekt zu bitten, eine Darstellung von sich selbst bereitzustellen, indem es auf einem vom Container angegebenen Gerätekontext gezeichnet wird.

Beim Aufrufen der [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) -Schnittstelle kann eine Containeranwendung auch angeben, dass sich das Objekt auf einem anderen Zielgerät als dem, auf dem es tatsächlich gerendert wird, zeichnen soll. Dies ermöglicht es dem Container nach Bedarf, unterschiedliche Renderings von einem einzelnen Objekt zu generieren. Der Aufrufer könnte das Objekt z. b. auffordern, sich selbst für einen Drucker zu verfassen, auch wenn die resultierende Zeichnung auf dem Bildschirm gerendert wird. Das Ergebnis ist natürlich eine Druckvorschau des Objekts.

Die [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)-Schnittstelle stellt auch Methoden bereit, mit denen sich Container für Ansichts Änderungs Benachrichtigungen registrieren können. Wie bei Daten-und OLE-Empfehlungen ermöglicht eine Ansichts Beratungs Verbindung einem Container, seine Renderings eines Objekts zu einem eigenen Zweck zu aktualisieren und nicht als Reaktion auf einen-Befehl aus dem-Objekt. Wenn z. b. eine neue Version der Serveranwendung eines Objekts zusätzliche Sichten derselben Daten bereitstellen würde, würde der Standard Handler des Objekts die Implementierung von [**IAdviseSink:: OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) für jeden Container aufrufen, um Sie darüber zu informieren, dass die neuen Präsentationen verfügbar waren. Der Container würde diese Informationen nur bei Bedarf von der Benachrichtigungs Senke abrufen.

Da Windows-Geräte Kontexte nur innerhalb eines einzelnen Prozesses Bedeutung haben, können Sie [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) -Zeiger nicht über Prozess Grenzen hinweg übergeben. Folglich haben OLE-lokale und Remote Server keine Notwendigkeit, die Schnittstelle zu implementieren, die selbst dann nicht ordnungsgemäß funktioniert, wenn dies der Fall war. Die **IViewObject2**-Schnittstelle wird nur von Objekt Handlern und Prozess internen Servern implementiert. OLE bietet eine Standard Implementierung, die Sie in ihren eigenen OLE-Prozess Servern und Objekt Handlern verwenden können, indem Sie einfach den OLE-Standard Handler aggregierten. Oder Sie können eine eigene Implementierung von **IViewObject2** schreiben.

Ein Objekt implementiert die [**iolecache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) -Schnittstelle, damit der Handler weiß, welche Funktionen zwischengespeichert werden sollen. Der Objekt Handler besitzt auch den Cache und stellt sicher, dass er auf dem neuesten Stand gehalten wird. Wenn das eingebettete Objekt in den Zustand "wird ausgeführt" wechselt, richtet der Handler entsprechende Beratungs Verbindungen für das Server Objekt ein, wobei er sich selbst als Senke verhält. Die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -und [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)-Schnittstellen Implementierungen arbeiten aus Daten, die auf der Clientseite zwischengespeichert werden. Die Implementierung von **IViewObject2** des Handlers ist dafür verantwortlich, zu bestimmen, welche Datenformate zwischengespeichert werden sollen, um Client Zeichnungs Anforderungen zu erfüllen. Die Implementierung von **IDataObject** des Handlers ist dafür verantwortlich, Daten in verschiedenen Formaten usw. zwischen Arbeitsspeicher und der zugrunde liegenden [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) -Instanz des eingebetteten Objekts zu erhalten. Benutzerdefinierte Handler können diese Implementierungen verwenden, indem Sie den Standard Handler aggregierten.

> [!Note]  
> Die [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) -Schnittstelle ist eine einfache funktionale Erweiterung von [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) und sollte anstelle der letzteren Schnittstelle implementiert werden, die mittlerweile veraltet ist. Zusätzlich zur Bereitstellung der **IViewObject** -Methoden bietet die **IViewObject2** -Schnittstelle ein einzelnes zusätzliches Element, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), das es einer Containeranwendung ermöglicht, die Größe der Darstellung eines Objekts aus dem Cache abzurufen, ohne dass das Objekt zuerst mit einem [**IOleObject:: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)-Befehl in den Ausführungs Zustand verschoben werden muss.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> </dl>

 

 