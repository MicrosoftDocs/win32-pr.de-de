---
title: Anzeigen der Zwischenspeicherung
description: Anzeigen der Zwischenspeicherung
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b155c0a9d3229db85a52b0589c4854bdee9a2e8e4171e231480036c512af737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047678"
---
# <a name="view-caching"></a>Anzeigen der Zwischenspeicherung

Eine Containeranwendung muss in der Lage sein, eine Darstellung eines Objekts zum Anzeigen oder Drucken für Benutzer zu erhalten, wenn das Dokument geöffnet ist, die Serveranwendung des Objekts jedoch nicht ausgeführt wird oder nicht auf dem Computer des Benutzers installiert ist. Es ist jedoch unrealistisch, davon auszugehen, dass die Server für alle Objekte, die sich möglicherweise in einem Dokument befinden, auf dem Computer jedes Benutzers installiert sind und immer bei Bedarf ausgeführt werden können. Der Standardobjekthandler, der jederzeit verfügbar ist, löst dieses Problem, indem er Objektpräsentationen im Speicher des Dokuments zwischenspeichert und diese Präsentationen auf jeder Plattform unabhängig von der Verfügbarkeit des Objektservers auf einer bestimmten Installation des Containers bearbeiten kann.

Container können Zeichnungspräsentationen für ein oder mehrere bestimmte Zielgeräte verwalten, zusätzlich zu dem, das zum Verwalten des Objekts auf dem Bildschirm erforderlich ist. Wenn Sie das Objekt von einer Plattform auf eine andere portieren, konvertiert OLE außerdem automatisch die Datenformate des Objekts in die formate, die auf der neuen Plattform unterstützt werden. Wenn Sie z. B. ein Objekt von Windows Macintosh verschieben, konvertiert OLE seine Metadateipräsentationen in PICT-Formate.

Um dem Benutzer eine genaue Darstellung eines eingebetteten Objekts zu präsentieren, initiiert die Containeranwendung des Objekts ein Dialogfeld mit dem Objekthandler, fordert Daten an und zeichent Anweisungen. Um die Anforderungen des Containers erfüllen zu können, muss der Handler die [**Schnittstellen IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)und [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) implementieren.

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ermöglicht einer OLE-Containeranwendung, Daten aus ihren eingebetteten oder verknüpften Objekten zu erhalten und an diese zu senden. Wenn sich Daten in einem Objekt ändern, bietet diese Schnittstelle dem Objekt eine Möglichkeit, seine neuen Daten für seinen Container verfügbar zu machen, und bietet dem Container die Möglichkeit, die Daten in seiner Kopie des Objekts zu aktualisieren. (Eine allgemeine Erörterung der Datenübertragung finden Sie in Kapitel 4, Datenübertragung.)

Die [**IViewObject2-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) ist sehr ähnlich wie die [**IDataObject-Schnittstelle,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) mit der Ausnahme, dass ein Objekt aufgefordert wird, sich selbst in einem Gerätekontext wie einem Bildschirm, Drucker oder metafile zu zeichnen, anstatt seine Daten in den Arbeitsspeicher oder ein anderes Übertragungsmedium zu verschieben oder zu kopieren. Der Zweck der -Schnittstelle besteht darin, einem OLE-Container das Abrufen alternativer darstellungsweiser Darstellungen seiner eingebetteten Objekte zu ermöglichen, deren Daten bereits vorhanden sind, wodurch der Aufwand vermieden wird, völlig neue Instanzen derselben Datenobjekte zu übertragen, um einfach neue Zeichnungsanweisungen zu erhalten. Stattdessen ermöglicht die **IViewObject2-Schnittstelle** dem Container, ein Objekt auf die Bereitstellung einer visuellen Darstellung von sich selbst zu bitten, indem er einen vom Container angegebenen Gerätekontext verwendet.

Beim Aufrufen der [**IViewObject2-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) kann eine Containeranwendung auch angeben, dass sich das Objekt auf einem anderen Zielgerät als dem, auf dem es tatsächlich gerendert wird, selbst zeichnen soll. Dadurch kann der Container bei Bedarf verschiedene Renderings aus einem einzelnen Objekt generieren. Beispielsweise könnte der Aufrufer das Objekt bitten, sich selbst für einen Drucker zu erstellen, obwohl die resultierende Zeichnung auf dem Bildschirm gerendert wird. Das Ergebnis wäre natürlich eine Druckvorschau des Objekts.

Die [**IViewObject2-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)stellt auch Methoden bereit, die es Containern ermöglichen, sich für Ansichtsänderungsbenachrichtigungen zu registrieren. Wie bei Daten- und OLE-Ratgebern ermöglicht eine Ansichtsempfehlungsverbindung einem Container das Aktualisieren seiner Renderings eines Objekts nach eigenem Komfort und nicht als Reaktion auf einen Aufruf des Objekts. Wenn beispielsweise eine neue Version der Serveranwendung eines Objekts zusätzliche Ansichten der gleichen Daten bietet, würde der Standardhandler des Objekts die Implementierung von [**IAdviseSink::OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) jedes Containers aufrufen, um sie darüber zu informieren, dass die neuen Präsentationen verfügbar sind. Der Container ruft diese Informationen nur bei Bedarf aus der Advise-Senke ab.

Da Windows Gerätekontexte nur innerhalb eines einzelnen Prozesses eine Bedeutung haben, können [**Sie IViewObject2-Zeiger**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) nicht über Prozessgrenzen hinweg übergeben. Daher ist es für lokale OLE- und Remoteserver nicht erforderlich, die -Schnittstelle zu implementieren, die auch dann nicht ordnungsgemäß funktioniert. Nur Objekthandler und Prozessserver implementieren die **IViewObject2-Schnittstelle.** OLE bietet eine Standardimplementierung, die Sie in Ihren eigenen OLE-Prozessservern und -Objekthandlern verwenden können, indem Sie einfach den OLE-Standardhandler aggregieren. Sie können auch eine eigene Implementierung von **IViewObject2 schreiben.**

Ein Objekt implementiert die [**IOleCache-Schnittstelle,**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) um den Handler darüber zu informieren, welche Funktionen zwischengespeichert werden sollen. Der Objekthandler besitzt auch den Cache und stellt sicher, dass er auf dem neuesten Stand gehalten wird. Wenn das eingebettete Objekt in den Ausführungszustand übergeht, richtet der Handler entsprechende Beratungsverbindungen für das Serverobjekt ein, bei denen er selbst als Senke agiert. Die [**IDataObject-**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) und [**IViewObject2-Schnittstellenimplementierungen**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)funktionieren aus Daten, die auf clientseitiger Seite zwischengespeichert sind. Die Implementierung von **IViewObject2** durch den Handler ist dafür verantwortlich, zu bestimmen, welche Datenformate zwischengespeichert werden müssen, um Client-Draw-Anforderungen zu erfüllen. Die Implementierung von **IDataObject** durch den Handler ist dafür verantwortlich, Daten in verschiedenen Formaten usw. zwischen dem Arbeitsspeicher und der zugrunde [**liegenden IStorage-Instanz**](/windows/desktop/api/objidl/nn-objidl-istorage) des eingebetteten Objekts zu erhalten. Benutzerdefinierte Handler können diese Implementierungen verwenden, indem sie den Standardhandler aggregieren.

> [!Note]  
> Die [**IViewObject2-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) ist eine einfache funktionale Erweiterung von [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) und sollte anstelle der zuletzt genannten Schnittstelle implementiert werden, die jetzt veraltet ist. Zusätzlich zur Bereitstellung der **IViewObject-Methoden** stellt die **IViewObject2-Schnittstelle** einen einzelnen zusätzlichen Member bereit, [**GetExtent,**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent)der es einer Containeranwendung ermöglicht, die Größe der Präsentation eines Objekts aus dem Cache zu erhalten, ohne zuerst das Objekt mit einem Aufruf von [**IOleObject::GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)in den Ausführungszustand verschieben zu müssen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbunddokumente](compound-documents.md)
</dt> </dl>

 

 