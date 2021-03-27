---
description: Viele Anwendungen ermöglichen es Benutzern, Daten in eine andere Anwendung zu übertragen, indem Sie die Daten mit der Maus ziehen und ablegen oder indem Sie die Zwischenablage verwenden.
title: Übertragen von shellobjekten mit Drag & Drop und der Zwischenablage
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979745"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Übertragen von shellobjekten mit Drag & Drop und der Zwischenablage

Viele Anwendungen ermöglichen es Benutzern, Daten in eine andere Anwendung zu übertragen, indem Sie die Daten mit der Maus ziehen und ablegen oder indem Sie die Zwischenablage verwenden. Zu den vielen Typen von Daten, die übertragen werden können, zählen Shellobjekte wie z. b. Dateien oder Ordner. Shell-Datenübertragungen können zwischen zwei Anwendungen erfolgen, Benutzer können jedoch auch shelldaten auf den oder den Desktop oder Windows-Explorer übertragen.

Obwohl es sich bei den Dateien um das am häufigsten übertragene Shellobjekt handelt, kann die Shell-Datenübertragung eine beliebige Anzahl von Objekten im [Shellnamespace](namespace-intro.md)enthalten. Beispielsweise muss Ihre Anwendung möglicherweise eine Datei in einen virtuellen Ordner, z. b. den Papierkorb, übertragen oder ein Objekt aus einer nicht von Microsoft abhängigen Namespace Erweiterung akzeptieren. Wenn Sie eine Namespace Erweiterung implementieren, muss Sie in der Lage sein, sich ordnungsgemäß als Drop Source und Target zu Verhalten.

In diesem Dokument wird erläutert, wie Anwendungen Drag & amp; Drop-und Zwischenablage-Datenübertragungen mit shellobjekten implementieren können.

-   [Das shelldatenobjekt](dataobject.md)
-   [Shellzwischenablage Formate](clipboard.md)
-   [Behandeln von Shelldatenübertragungs-Szenarien](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Funktionsweise von Drag & amp; Drop mit shellobjekten

Anwendungen müssen häufig den Benutzern eine Möglichkeit zum Übertragen von shelldaten bieten. Hier einige Beispiele:

-   Ziehen Sie eine Datei aus Windows Explorer oder dem Desktop, und löschen Sie Sie in einer Anwendung.
-   Kopieren einer Datei in die Zwischenablage in Windows-Explorer und Einfügen in eine Anwendung.
-   Ziehen einer Datei aus einer Anwendung in den Papierkorb.

Ausführliche Informationen zur Handhabung dieser und anderer Szenarien finden Sie unter [Handling Shell Datenübertragung Szenarios](datascenarios.md). Dieses Dokument konzentriert sich auf die allgemeinen Prinzipien hinter der Shell-Datenübertragung.

Windows bietet zwei Standardmethoden für die Übertragung von shelldaten durch Anwendungen:

-   Ein Benutzer schneidet shelldaten (z. b. eine oder mehrere Dateien) in der Zwischenablage ab oder kopiert sie. Die andere Anwendung ruft die Daten aus der Zwischenablage ab.
-   Ein Benutzer zieht ein Symbol, das die Daten aus der Quell Anwendung darstellt, und löscht das Symbol in einem Fenster, das dem Ziel gehört.

In beiden Fällen sind die übertragenen Daten in einem *Datenobjekt* enthalten. Datenobjekte sind Component Object Model (com)-Objekte, die die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle verfügbar machen. Schematisch gibt es drei wesentliche Schritte, die alle shelldatenübertragungen ausführen müssen:

1.  Die Quelle erstellt ein Datenobjekt, das die zu übertragenden Daten darstellt.
2.  Das Ziel erhält einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts.
3.  Das Ziel Ruft die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle auf, um die Daten daraus zu extrahieren.

Der Unterschied zwischen der Zwischenablage und den Drag & Drop-Datenübertragungen liegt in erster Linie darin, wie der [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger von der Quelle zum Ziel übertragen wird.

### <a name="clipboard-data-transfers"></a>Zwischenablage-Datenübertragungen

Die Zwischenablage ist die einfachste Methode zum Übertragen von shelldaten. Das grundlegende Verfahren ähnelt den standardmäßigen Zwischenablage Datenübertragungen. Da Sie jedoch einen Zeiger auf ein Datenobjekt, nicht die Daten selbst, übertragen, müssen Sie die OLE-Zwischenablage-API anstelle der Standard-Zwischenablage-API verwenden. Im folgenden Verfahren wird erläutert, wie die OLE-Zwischenablage-API zum Übertragen von shelldaten mit der Zwischenablage verwendet wird:

1.  Die Datenquelle erstellt ein Datenobjekt, das die Daten enthält.
2.  Die Datenquelle ruft [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard)auf, wodurch ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts in der Zwischenablage platziert wird.
3.  Das Ziel ruft [**olegetclipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) auf, um den Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts abzurufen.
4.  Das Ziel extrahiert die Daten, indem die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode aufgerufen wird.
5.  Bei einigen shelldatenübertragungen muss das Ziel möglicherweise auch die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts aufrufen, um dem Datenobjekt für das Ergebnis der Datenübertragung Feedback zu geben. Ein Beispiel für diese Art von Vorgang finden Sie unter [Handling optimierte](datascenarios.md) Verschiebungs Vorgänge.

### <a name="drag-and-drop-data-transfers"></a>Datenübertragungen per Drag & Drop

Die Datenübertragung mit Drag & Drop ist zwar etwas komplexer, bietet jedoch einige bedeutende Vorteile gegenüber der Zwischenablage:

-   Drag & Drop-Übertragungen können mit einer einfachen Mausbewegung durchgeführt werden, sodass der Betrieb flexibler und intuitiver ist als die Zwischenablage.
-   Durch Drag & amp; Drop erhält der Benutzer eine visuelle Darstellung des Vorgangs. Der Benutzer kann dem Symbol folgen, wenn es von der Quelle zum Ziel wechselt.
-   Durch Drag & amp; Drop wird das Ziel benachrichtigt, wenn die Daten verfügbar sind.

Bei Drag & Drop-Vorgängen werden auch Datenobjekte verwendet, um Daten zu übertragen. Allerdings muss die Drop-Quelle über die für Zwischenablage Übertragungen erforderliche Funktionalität hinaus bereitstellen:

-   Die Drop-Quelle muss außerdem ein Objekt erstellen, das eine [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht. Das System verwendet **IDropSource** , um mit der Quelle zu kommunizieren, während der Vorgang ausgeführt wird.
-   Das Drag & amp; Drop-Datenobjekt ist für die Überwachung der Cursor Bewegung und die Anzeige eines Symbols zur Darstellung des Datenobjekts verantwortlich.

Drop Targets muss auch mehr Funktionalität bereitstellen, als für die Verarbeitung von Zwischenablage Übertragungen erforderlich ist:

-   Das Ablage Ziel muss eine [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle verfügbar machen. Wenn sich der Cursor über einem Zielfenster befindet, verwendet das System **IDropTarget** , um dem Ziel Informationen, wie z. b. die Cursorposition, bereitzustellen und Sie zu benachrichtigen, wenn die Daten gelöscht werden.
-   Das Ablage Ziel muss sich selbst beim System registrieren, indem [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop)aufgerufen wird. Diese Funktion stellt dem System das Handle für ein Zielfenster und einen Zeiger auf die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle der Zielanwendung bereit.

> [!Note]  
> Bei Drag & Drop-Vorgängen muss Ihre Anwendung com mit [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize)initialisieren, nicht mit [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

Im folgenden Verfahren werden die wesentlichen Schritte erläutert, die in der Regel zum Übertragen von shelldaten per Drag & Drop verwendet werden:

1.  Das Ziel ruft [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) auf, um dem System einen Zeiger auf seine [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle zu übergeben und ein Fenster als Ablage Ziel zu registrieren.
2.  Wenn der Benutzer einen Drag & Drop-Vorgang startet, erstellt die Quelle ein Datenobjekt und initiiert eine *Drag-Schleife* durch Aufrufen von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Wenn sich der Cursor über dem Zielfenster befindet, benachrichtigt das System das Ziel, indem es eine der [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Methoden des Ziels aufruft. Das System ruft [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) auf, wenn der Cursor das Zielfenster eingibt, und [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) , wenn der Cursor über das Zielfenster bewegt wird. Beide Methoden stellen das Ablage Ziel mit der aktuellen Cursorposition und dem Zustand von Tastatur-modifiziererschlüsseln, wie z. b. STRG oder alt, bereit. Wenn der Cursor das Zielfenster verlässt, benachrichtigt das System das Ziel durch Aufrufen von [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Wenn eine dieser Methoden zurückgibt, ruft das System die [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle auf, um den Rückgabewert an die Quelle zu übergeben.
4.  Wenn der Benutzer die Maustaste loslässt, um die Daten zu löschen, ruft das System die [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode des Ziels auf. Neben den Parametern der Methode ist ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts.
5.  Das Ziel Ruft die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode des Datenobjekts auf, um die Daten zu extrahieren.
6.  Bei einigen shelldatenübertragungen muss das Ziel möglicherweise auch die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode des Datenobjekts aufrufen, um der Quelle Feedback für das Ergebnis der Datenübertragung zu geben.
7.  Wenn das Ziel mit dem Datenobjekt fertig ist, wird es von [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop)zurückgegeben. Das System gibt den [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) -Anrufe der Quelle zurück, um die Quelle zu benachrichtigen, dass die Datenübertragung beendet ist.
8.  Abhängig vom jeweiligen [Datenübertragungs Szenario](datascenarios.md)muss die Quelle möglicherweise zusätzliche Maßnahmen ergreifen, basierend auf dem von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) zurückgegebenen Wert und den Werten, die vom Ziel an das Datenobjekt übergeben werden. Wenn beispielsweise eine Datei verschoben wird, muss die Quelle diese Werte überprüfen, um zu bestimmen, ob Sie die ursprüngliche Datei löschen muss.
9.  Die Quelle gibt das Datenobjekt frei.

Obwohl die oben beschriebenen Prozeduren ein gutes allgemeines Modell für Shell-Datenübertragungen darstellen, gibt es viele verschiedene Arten von Daten, die in einem shelldatenobjekt enthalten sein können. Es gibt auch eine Reihe verschiedener Datenübertragungs Szenarien, die Ihre Anwendung möglicherweise verarbeiten muss. Jeder Datentyp und jedes Szenario erfordert einen etwas anderen Ansatz für drei wichtige Schritte in der Prozedur:

-   Gibt an, wie eine Quelle ein Datenobjekt erstellt, das die shelldaten enthalten soll.
-   Gibt an, wie ein Ziel shelldaten aus dem Datenobjekt extrahiert.
-   Gibt an, wie der Daten Übertragungsvorgang von der Quelle abgeschlossen wird.

Das [Shell-Datenobjekt](dataobject.md) bietet eine allgemeine Erörterung der Art und Weise, wie eine Quelle ein shelldatenobjekt erstellt und wie dieses Datenobjekt vom Ziel behandelt werden kann. Bei der [Behandlung von Shell-Datenübertragung Szenarios](datascenarios.md) wird ausführlich erläutert, wie eine Reihe allgemeiner Shell-Datenübertragungs Szenarien behandelt werden.

 

 
