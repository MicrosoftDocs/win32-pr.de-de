---
description: Viele Anwendungen ermöglichen Es Benutzern, Daten in eine andere Anwendung zu übertragen, indem sie die Daten mit der Maus ziehen und ablegen oder die Zwischenablage verwenden.
title: Übertragen von Shellobjekten mit Drag & Drop und der Zwischenablage
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c45fc01709c50fd309c285cb486474cab2f1d8ac0b20c56bb7e21578cb8138f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090620"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Übertragen von Shellobjekten mit Drag & Drop und der Zwischenablage

Viele Anwendungen ermöglichen Es Benutzern, Daten in eine andere Anwendung zu übertragen, indem sie die Daten mit der Maus ziehen und ablegen oder die Zwischenablage verwenden. Zu den vielen Arten von Daten, die übertragen werden können, gehören Shellobjekte wie Dateien oder Ordner. Die Shell-Datenübertragung kann zwischen zwei Anwendungen stattfinden, benutzer können jedoch auch Shelldaten an den oder vom Desktop oder Windows übertragen.

Obwohl Dateien das am häufigsten übertragene Shellobjekt sind, kann die Shell-Datenübertragung jede der verschiedenen Objekte umfassen, die sich im [Shellnamespace befinden.](namespace-intro.md) Beispielsweise muss Ihre Anwendung möglicherweise eine Datei in einen virtuellen Ordner wie den Papierkorb übertragen oder ein Objekt von einer Nicht-Microsoft-Namespaceerweiterung akzeptieren. Wenn Sie eine Namespaceerweiterung implementieren, muss sie sich als Absturzquelle und -ziel ordnungsgemäß verhalten können.

In diesem Dokument wird erläutert, wie Anwendungen Drag & Drop- und Zwischenablagedatenübertragungen mit Shellobjekten implementieren können.

-   [Das Shell-Datenobjekt](dataobject.md)
-   [Shell-Zwischenablageformate](clipboard.md)
-   [Behandeln von Shelldatenübertragungs-Szenarien](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Funktionsweise von Drag & Drop mit Shellobjekten

Anwendungen müssen Benutzern häufig eine Möglichkeit bieten, Shelldaten zu übertragen. Beispiele:

-   Ziehen einer Datei aus Windows explorer oder dem Desktop und Ablegen in einer Anwendung.
-   Kopieren einer Datei in die Zwischenablage in Windows Explorer und Ein eingefügt in eine Anwendung.
-   Ziehen einer Datei aus einer Anwendung in den Papierkorb.

Eine ausführliche Erläuterung des Umgangs mit diesen und anderen Szenarien finden Sie unter [Handling Shell Data Transfer Scenarios](datascenarios.md). Dieses Dokument konzentriert sich auf die allgemeinen Prinzipien der Shell-Datenübertragung.

Windows bietet zwei Standardverfahren für Anwendungen zum Übertragen von Shelldaten:

-   Ein Benutzer schneidet Shelldaten, z. B. eine oder mehrere Dateien, aus oder kopiert sie in die Zwischenablage. Die andere Anwendung ruft die Daten aus der Zwischenablage ab.
-   Ein Benutzer zieht ein Symbol, das die Daten aus der Quellanwendung darstellt, und löscht das Symbol in einem Fenster, das sich im Besitz des Ziels befindet.

In beiden Fällen sind die übertragenen Daten in einem *Datenobjekt enthalten.* Datenobjekte sind Component Object Model (COM), die die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) verfügbar machen. Schematisch gibt es drei wesentliche Schritte, die alle Shell-Datenübertragungen ausführen müssen:

1.  Die Quelle erstellt ein Datenobjekt, das die zu übertragenden Daten darstellt.
2.  Das Ziel empfängt einen Zeiger auf die [**IDataObject-Schnittstelle des**](/windows/win32/api/objidl/nn-objidl-idataobject) Datenobjekts.
3.  Das Ziel ruft die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) auf, um die Daten daraus zu extrahieren.

The difference between Clipboard and drag-and-drop data transfers lies primarily in how the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer is transferred from the source to the target.

### <a name="clipboard-data-transfers"></a>Datenübertragungen in der Zwischenablage

Die Zwischenablage ist die einfachste Möglichkeit zum Übertragen von Shelldaten. Das grundlegende Verfahren ähnelt den standardmäßigen Zwischenablage-Datenübertragungen. Da Sie jedoch einen Zeiger auf ein Datenobjekt und nicht auf die Daten selbst übertragen, müssen Sie die OLE-Zwischenablage-API anstelle der Standard-Zwischenablage-API verwenden. Im folgenden Verfahren wird beschrieben, wie Sie die OLE-Zwischenablage-API verwenden, um Shelldaten mit der Zwischenablage zu übertragen:

1.  Die Datenquelle erstellt ein Datenobjekt, das die Daten enthalten soll.
2.  Die Datenquelle ruft [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard)auf, wodurch ein Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts in der Zwischenablage platziert wird.
3.  Das Ziel ruft [**OleGetClipboard auf,**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) um den Zeiger auf die [**IDataObject-Schnittstelle des Datenobjekts**](/windows/win32/api/objidl/nn-objidl-idataobject) abzurufen.
4.  Das Ziel extrahiert die Daten durch Aufrufen der [**IDataObject::GetData-Methode.**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)
5.  Bei einigen Shell-Datenübertragungen muss das Ziel möglicherweise auch die [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) des Datenobjekts aufrufen, um dem Datenobjekt Feedback zum Ergebnis der Datenübertragung zu geben. Ein Beispiel für diese Art von Vorgang finden Sie unter Handling [Optimized Move Operations](datascenarios.md) (Behandeln optimierter Verschieben-Vorgänge).

### <a name="drag-and-drop-data-transfers"></a>Drag & Drop-Datenübertragungen

Obwohl die Implementierung etwas komplexer ist, bietet die Drag & Drop-Datenübertragung einige erhebliche Vorteile gegenüber der Zwischenablage:

-   Drag & Drop-Übertragungen können mit einer einfachen Mausbewegung durchgeführt werden, wodurch der Betrieb flexibler und intuitiver zu verwenden ist als die Zwischenablage.
-   Drag & Drop bietet dem Benutzer eine visuelle Darstellung des Vorgangs. Der Benutzer kann dem Symbol folgen, während es von der Quelle zum Ziel wechselt.
-   Drag & Drop benachrichtigt das Ziel, wenn die Daten verfügbar sind.

Drag & Drop-Vorgänge verwenden auch Datenobjekte, um Daten zu übertragen. Die Ablagequelle muss jedoch funktionen bereitstellen, die über die für Zwischenablageübertragungen erforderliche Funktionalität hinausgehen:

-   Die Absturzquelle muss auch ein Objekt erstellen, das eine [**IDropSource-Schnittstelle verfügbar**](/windows/win32/api/oleidl/nn-oleidl-idropsource) macht. Das System verwendet **IDropSource** für die Kommunikation mit der Quelle, während der Vorgang läuft.
-   Das Drag & Drop-Datenobjekt ist für das Nachverfolgen der Cursorbewegung und das Anzeigen eines Symbols zur Darstellung des Datenobjekts verantwortlich.

Ablageziele müssen auch mehr Funktionalität bieten, als für die Übertragung der Zwischenablage erforderlich ist:

-   Das Abbruchziel muss eine [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) verfügbar machen. Wenn sich der Cursor über einem Zielfenster befindet, verwendet das System **IDropTarget,** um dem Ziel Informationen wie die Cursorposition zur Verfügung zu stellen und es zu benachrichtigen, wenn die Daten gelöscht werden.
-   Das Abbruchziel muss sich durch Aufrufen von [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop)selbst beim System registrieren. Diese Funktion stellt dem System das Handle für ein Zielfenster und einen Zeiger auf die [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) der Zielanwendung bereit.

> [!Note]  
> For drag-and-drop operations, your application must initialize COM with [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), not [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

Im folgenden Verfahren werden die wesentlichen Schritte beschrieben, die normalerweise zum Übertragen von Shelldaten mit Drag & Drop verwendet werden:

1.  Das Ziel ruft [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) auf, um dem System einen Zeiger auf seine [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) zu geben und ein Fenster als Absturzziel zu registrieren.
2.  When the user starts a drag-and-drop operation, the source creates a data object and initiates a *drag loop* by calling [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Wenn sich der Cursor über dem Zielfenster befindet, benachrichtigt das System das Ziel, indem es eine der [**IDropTarget-Methoden des Ziels**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) aufruft. Das System ruft [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) auf, wenn der Cursor in das Zielfenster eintritt, und [**IDropTarget::D ragOver,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) wenn der Cursor das Zielfenster übergibt. Beide Methoden stellen das Ablageziel mit der aktuellen Cursorposition und dem Zustand von Tastaturmodifizierertasten wie STRG oder ALT zur Verfügung. Wenn der Cursor das Zielfenster verlässt, benachrichtigt das System das Ziel, indem es [**IDropTarget::D ragLeave aufruft.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) Wenn eine dieser Methoden zurücksingt, ruft das System die [**IDropSource-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idropsource) auf, um den Rückgabewert an die Quelle zu übergeben.
4.  Wenn der Benutzer die Maustaste loslässt, um die Daten zu löschen, ruft das System die [**IDropTarget::D rop-Methode des Ziels**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) auf. Zu den Parametern der Methode gehört ein Zeiger auf die [**IDataObject-Schnittstelle des Datenobjekts.**](/windows/win32/api/objidl/nn-objidl-idataobject)
5.  Das Ziel ruft die [**IDataObject::GetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) des Datenobjekts auf, um die Daten zu extrahieren.
6.  Bei einigen Shell-Datenübertragungen muss das Ziel möglicherweise auch die [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) des Datenobjekts aufrufen, um der Quelle Feedback zum Ergebnis der Datenübertragung zu geben.
7.  Wenn das Ziel mit dem Datenobjekt fertig ist, wird von [**IDropTarget::D rop zurückgegeben.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) Das System gibt den [**DoDragDrop-Aufruf**](/windows/win32/api/ole2/nf-ole2-dodragdrop) der Quelle zurück, um die Quelle zu benachrichtigen, dass die Datenübertragung abgeschlossen ist.
8.  Abhängig vom jeweiligen [](datascenarios.md)Datenübertragungsszenario muss die Quelle möglicherweise zusätzliche Maßnahmen ergreifen, die auf dem von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) zurückgegebenen Wert und den Werten basieren, die vom Ziel an das Datenobjekt übergeben werden. Wenn beispielsweise eine Datei verschoben wird, muss die Quelle diese Werte überprüfen, um zu bestimmen, ob die ursprüngliche Datei gelöscht werden muss.
9.  Die Quelle gibt das Datenobjekt frei.

Obwohl die oben beschriebenen Verfahren ein gutes allgemeines Modell für die Shell-Datenübertragung bieten, gibt es viele verschiedene Datentypen, die in einem Shell-Datenobjekt enthalten sein können. Es gibt auch eine Reihe verschiedener Datenübertragungsszenarien, die Ihre Anwendung möglicherweise verarbeiten muss. Jeder Datentyp und jedes Szenario erfordert einen etwas anderen Ansatz als drei wichtige Schritte in der Prozedur:

-   Wie eine Quelle ein Datenobjekt erstellt, das die Shelldaten enthalten soll.
-   Wie ein Ziel Shelldaten aus dem Datenobjekt extrahiert.
-   Wie die Quelle den Datenübertragungsvorgang ab schließt.

Das [Shell-Datenobjekt](dataobject.md) bietet eine allgemeine Diskussion darüber, wie eine Quelle ein Shell-Datenobjekt erstellt und wie dieses Datenobjekt vom Ziel behandelt werden kann. [Unter Handling Shell Data Transfer Scenarios](datascenarios.md) (Behandeln von Shell-Datenübertragungsszenarien) wird ausführlich erläutert, wie eine Reihe gängiger Shell-Datenübertragungsszenarien behandelt werden.

 

 
