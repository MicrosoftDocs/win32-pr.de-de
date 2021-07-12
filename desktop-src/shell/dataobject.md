---
description: Das Datenobjekt ist für alle Shell-Datenübertragungen von zentraler Bedeutung.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Shelldatenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a6c411310b6c9e9f28df4de048d3b6909c44b9
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581628"
---
# <a name="shell-data-object"></a>Shelldatenobjekt

Das Datenobjekt ist für alle Shell-Datenübertragungen von zentraler Bedeutung. Es handelt sich in erster Linie um einen Container, in dem die übertragenen Daten gespeichert werden. Das Ziel kann jedoch auch mit dem Datenobjekt kommunizieren, um einige spezialisierte Typen der Shell-Datenübertragung zu ermöglichen, z. B. optimierte Verschiebebewegungen. In diesem Thema wird allgemein beschrieben, wie Shell-Datenobjekte funktionieren, wie sie von einer Quelle erstellt werden und wie sie von einem Ziel behandelt werden. Eine ausführliche Erläuterung der Verwendung von Datenobjekten zum Übertragen verschiedener Typen von Shelldaten finden Sie unter [Behandeln von Shell-Datenübertragungsszenarien.](datascenarios.md)

-   [Funktionsweise von Datenobjekten](#how-data-objects-work)
    -   [Zwischenablageformate](#clipboard-formats)
    -   [FORMATETC-Struktur](#formatetc-structure)
    -   [STGMEDIUM-Struktur](#stgmedium-structure)
-   [Erstellen eines Datenobjekts durch eine Quelle](#how-a-source-creates-a-data-object)
    -   [Hinzufügen eines globalen Speicherobjekts zu einem Datenobjekt](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementieren von IDataObject](#implementing-idataobject)
    -   [Implementieren von IDropSource](#implementing-idropsource)
-   [So behandelt ein Ziel ein Datenobjekt](#how-a-target-handles-a-data-object)
    -   [Extrahieren von Shelldaten aus einem Datenobjekt](#extracting-shell-data-from-a-data-object)
    -   [Implementieren von IDropTarget](#implementing-idroptarget)
-   [Using the Drag-and-Drop Helper Object](#using-the-drag-and-drop-helper-object)
    -   [Verwenden der IDragSourceHelper-Schnittstelle](#using-the-idragsourcehelper-interface)
    -   [Verwenden der IDropTargetHelper-Schnittstelle](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Funktionsweise von Datenobjekten

Datenobjekte sind Component Object Model (COM)-Objekte, die von der Datenquelle erstellt wurden, um Daten an ein Ziel zu übertragen. Sie enthalten in der Regel mehr als ein Datenelement. Für diese Vorgehensweise gibt es zwei Gründe:

-   Obwohl fast jede Art von Daten mit einem Datenobjekt übertragen werden kann, weiß die Quelle in der Regel nicht, welche Art von Daten das Ziel akzeptieren kann. Beispielsweise können die Daten ein Teil eines formatierten Textdokuments sein. Obwohl das Ziel möglicherweise komplexe Formatierungsinformationen verarbeiten kann, kann es auch nur ANSI-Text akzeptieren. Aus diesem Grund enthalten Datenobjekte häufig dieselben Daten in verschiedenen Formaten. Das Ziel kann die Daten dann in einem Format extrahieren, das es verarbeiten kann.
-   Datenobjekte können auch zusätzliche Datenelemente enthalten, die keine Versionen der Quelldaten sind. Diese Art von Datenelement stellt in der Regel zusätzliche Informationen zum Datenübertragungsvorgang zur Verfügung. Beispielsweise verwendet die Shell zusätzliche Datenelemente, um anzugeben, ob eine Datei kopiert oder verschoben werden soll.

### <a name="clipboard-formats"></a>Zwischenablageformate

Jedem Datenelement in einem Datenobjekt ist ein Format zugeordnet, das in der Regel als *Zwischenablageformat bezeichnet wird.* Es gibt eine Reihe von Standardformaten für die Zwischenablage, die in Winuser.h deklariert sind und häufig verwendeten Datentypen entsprechen. Zwischenablageformate sind ganze Zahlen, aber normalerweise wird auf sie durch ihren entsprechenden Namen verwiesen, der die Form CF \_ *XXX hat.* Das Zwischenablageformat für ANSI-Text ist beispielsweise CF \_ TEXT.

Anwendungen können den Bereich der verfügbaren Zwischenablageformate erweitern, indem sie private Formate definieren. Um ein privates Format zu definieren, ruft eine Anwendung [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) mit einer Zeichenfolge auf, die das Format identifiziert. Die ganze Zahl ohne Vorzeichen, die die Funktion zurückgibt, ist ein gültiger Formatwert, der genau wie ein Standardformat für die Zwischenablage verwendet werden kann. Allerdings müssen sowohl quelle als auch target das Format registrieren, um es verwenden zu können. Mit einer Ausnahme–[CF \_ HDROP](clipboard.md)– werden die Zwischenablageformate, die zum Übertragen von Shelldaten verwendet werden, als private Formate definiert. Sie müssen von der Quelle und dem Ziel registriert werden, bevor sie verwendet werden können. Eine Beschreibung der verfügbaren Shell-Zwischenablageformate finden Sie unter Shell-Zwischenablageformate.

Obwohl es einige Ausnahmen gibt, enthalten Datenobjekte normalerweise nur ein Datenelement für jedes von ihnen unterstützte Zwischenablageformat. Diese 1:1-Korrelation zwischen Format und Daten ermöglicht die Verwendung des Formatwerts als Bezeichner für das zugeordnete Datenelement. Bei der Erörterung des Inhalts eines Datenobjekts wird ein bestimmtes Datenelement in der Regel als "Format" bezeichnet und durch seinen Formatnamen bezeichnet. Beispiele hierfür sind Ausdrücke wie "Extrahieren des \_ CF-TEXTformats...". werden in der Regel verwendet, wenn das ANSI-Textdatenelement eines Datenobjekts diskutiert wird.

Wenn das Abbruchziel den Zeiger auf das Datenobjekt empfängt, werden die verfügbaren Formate aufzählt, um zu bestimmen, welche Datentypen verfügbar sind. Anschließend werden eines oder mehrere der verfügbaren Formate anfordern und die Daten extrahiert. Die spezifische Art und Weise, wie das Ziel Shelldaten aus einem Datenobjekt extrahiert, variiert je nach Format. Dies wird ausführlich unter Verarbeiten eines [Datenobjekts](#how-a-target-handles-a-data-object)durch ein Ziel erläutert.

Bei einfachen Datenübertragungen in der Zwischenablage werden die Daten in einem globalen Speicherobjekt platziert. Die Adresse dieses Objekts wird zusammen mit seinem Format in der Zwischenablage platziert. Das Format der Zwischenablage teilt dem Ziel mit, welche Art von Daten es an der zugeordneten Adresse findet. Während einfache Zwischenablageübertragungen einfach zu implementieren sind:

-   Datenobjekte bieten eine wesentlich flexiblere Möglichkeit zum Übertragen von Daten.
-   Datenobjekte eignen sich besser für die Übertragung großer Datenmengen.
-   Datenobjekte müssen zum Übertragen von Daten mit einem Drag & Drop-Vorgang verwendet werden.

Aus diesen Gründen verwenden alle Shell-Datenübertragungen Datenobjekte. Bei Datenobjekten werden Zwischenablageformate nicht direkt verwendet. Stattdessen werden Datenelemente mit einer Generalisierung des Zwischenablageformats identifiziert, einer [**FORMATETC-Struktur.**](/windows/win32/api/objidl/ns-objidl-formatetc)

### <a name="formatetc-structure"></a>FORMATETC-Struktur

Die [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) ist eine erweiterte Version eines Zwischenablageformats. Wie bei Shell-Datenübertragungen verwendet, hat die **FORMATETC-Struktur** die folgenden Merkmale:

-   Ein Datenelement wird weiterhin durch sein Zwischenablageformat im **cfFormat-Element** identifiziert.
-   Die Datenübertragung ist nicht auf globale Speicherobjekte beschränkt. Das **tymed-Member** wird verwendet, um den Datenübertragungsmechanismus anzugeben, der in der zugeordneten [**STGMEDIUM-Struktur enthalten**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) ist. Sie ist auf einen der [**TYMED \_ XXX-Werte**](/windows/win32/api/objidl/ne-objidl-tymed) festgelegt.
-   Die Shell verwendet den **lIndex-Member** mit seinem [CFSTR \_ FILECONTENTS-Format,](clipboard.md) damit ein Datenobjekt mehr als ein Datenelement pro Format enthalten kann. Eine Erörterung der Verwendung dieses Formats finden Sie im Abschnitt Using the CFSTR FILECONTENTS Format to Extract Data from a File (Verwenden des *CFSTR \_ FILECONTENTS-Formats* zum Extrahieren von Daten aus einer Datei) unter Handling Shell Data Transfer Scenarios (Behandeln von [Shell-Datenübertragungsszenarien).](datascenarios.md)
-   Das **dwAspect-Member** ist in der Regel auf DVASPECT \_ CONTENT festgelegt. In Shlobj.h sind jedoch drei Werte definiert, die für die Shell-Datenübertragung verwendet werden können. 

    | Wert               | BESCHREIBUNG                                                                                       |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | DVASPECT \_ COPY      | Wird verwendet, um anzugeben, dass das Format eine Kopie der Daten darstellt.                                   |
    | DVASPECT-LINK \_      | Wird verwendet, um anzugeben, dass das Format eine Verknüpfung mit den Daten darstellt.                               |
    | DVASPECT \_ SHORTNAME | Wird mit dem CF HDROP-Format verwendet, um einen Dateipfad mit den Namen an fordern, die \_ auf das 8.3-Format verkürzt sind. |

    

     

-   Der **ptd-Member** wird nicht für Shell-Datenübertragungen verwendet und ist normalerweise auf **NULL festgelegt.**

### <a name="stgmedium-structure"></a>STGMEDIUM-Struktur

Die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) ermöglicht den Zugriff auf die übertragenen Daten. Für Shelldaten werden drei Datenübertragungsmechanismen unterstützt:

-   Ein globales Speicherobjekt.
-   Eine [**IStream-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-istream)
-   Eine [**IStorage-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-istorage)

Das **tymed-Member** der [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) ist ein [**TYMED \_ XXX-Wert,**](/windows/win32/api/objidl/ne-objidl-tymed) der den Datenübertragungsmechanismus identifiziert. Der zweite Member ist ein Zeiger, der vom Ziel zum Extrahieren der Daten verwendet wird. Der Zeiger kann je nach **tyd-Wert** einer der verschiedenen Typen sein. Die drei für Shell-Datenübertragungen verwendeten **tymed-Werte** werden in der folgenden Tabelle zusammen mit dem entsprechenden **STGMEDIUM-Membernamen** zusammengefasst.



| tymed Value     | Membername | Beschreibung                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | Ein Zeiger auf ein globales Speicherobjekt. Dieser Zeigertyp wird in der Regel zum Übertragen kleiner Datenmengen verwendet. Beispielsweise verwendet die Shell globale Speicherobjekte, um kurze Textzeichenfolgen wie Dateinamen oder URLs zu übertragen.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Ein Zeiger auf eine [**IStream-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-istream) Dieser Zeigertyp wird für die meisten Shell-Datenübertragungen bevorzugt, da er im Vergleich zu TYMED CABLOBAL relativ wenig Arbeitsspeicher \_ erfordert. Darüber hinaus erfordert der TYMED \_ ISTREAM-Datenübertragungsmechanismus nicht, dass die Quelle ihre Daten auf eine bestimmte Weise speichert. |
| TYMED \_ ISTORAGE | **pstg**    | Ein Zeiger auf eine [**IStorage-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-istorage) Das Ziel ruft die Schnittstellenmethoden auf, um die Daten zu extrahieren. Wie TYMED \_ ISTREAM erfordert dieser Zeigertyp relativ wenig Arbeitsspeicher. Da TYMED \_ ISTORAGE jedoch weniger flexibel als TYMED \_ ISTREAM ist, wird es nicht so häufig verwendet.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Erstellen eines Datenobjekts durch eine Quelle

Wenn ein Benutzer eine Shell-Datenübertragung initiiert, ist die Quelle dafür verantwortlich, ein Datenobjekt zu erstellen und mit Daten zu laden. Im folgenden Verfahren wird der Prozess zusammengefasst:

1.  Rufen Sie [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) auf, um einen gültigen Zwischenablageformatwert für jedes Shellformat abzurufen, das im Datenobjekt enthalten ist. Beachten Sie, dass [CF \_ HDROP](clipboard.md) bereits ein gültiges Zwischenablageformat ist und nicht registriert werden muss.
2.  Legen Sie für jedes zu übertragende Format entweder die zugeordneten Daten in ein globales Speicherobjekt ab, oder erstellen Sie ein Objekt, das über eine [**IStream-**](/windows/win32/api/objidl/nn-objidl-istream) oder [**IStorage-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-istorage) Zugriff auf diese Daten bietet. Die **IStream-** und **IStorage-Schnittstellen** werden mit com-Standardtechniken erstellt. Eine Erläuterung des Umgangs mit globalen Speicherobjekten finden Sie unter [Hinzufügen eines globalen Speicherobjekts zu einem Datenobjekt.](#how-to-add-a-global-memory-object-to-a-data-object)
3.  Erstellen Sie [**FORMATETC-**](/windows/win32/api/objidl/ns-objidl-formatetc) und [**STGMEDIUM-Strukturen**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) für jedes Format.
4.  Instanziieren sie ein Datenobjekt.
5.  Laden Sie die Daten in das Datenobjekt, indem Sie die [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) für jedes unterstützte Format aufrufen und die [**FORMATETC-**](/windows/win32/api/objidl/ns-objidl-formatetc) und [**STGMEDIUM-Strukturen**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) des Formats übergeben.
6.  Rufen Sie bei Datenübertragungen in der Zwischenablage [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) auf, um einen Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts in der Zwischenablage zu platzieren. For drag-and-drop transfers, initiate a *drag loop* by calling [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). Der **IDataObject-Zeiger** wird an das Ablageziel übergeben, wenn die Daten gelöscht werden, um die Ziehschleife zu beenden.

Das Datenobjekt kann jetzt an das Ziel übertragen werden. Bei Datenübertragungen in der Zwischenablage wird das Objekt einfach so lange aufbewahrt, bis es vom Ziel angefordert wird, indem [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)aufgerufen wird. Bei Drag & Drop-Datenübertragungen ist das Datenobjekt dafür verantwortlich, ein Symbol zu erstellen, das die Daten darstellt und beim Bewegen des Cursors durch den Benutzer verschiebt. Während sich das Objekt in der Ziehschleife befindet, empfängt die Quelle Statusinformationen über die [**IDropSource-Schnittstelle.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Weitere Informationen finden Sie unter [Implementieren von IDropSource](#implementing-idropsource).

Die Quelle empfängt keine Benachrichtigung, wenn das Datenobjekt von einem Ziel aus der Zwischenablage abgerufen wird. When an object is dropped on a target by a drag-and-drop operation, the [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) function that was called to initiate the drag loop will return.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Hinzufügen eines globalen Speicherobjekts zu einem Datenobjekt

Viele der Shell-Datenformate haben die Form eines globalen Speicherobjekts. Verwenden Sie das folgende Verfahren, um ein Format zu erstellen, das ein globales Speicherobjekt enthält, und laden Sie es in das Datenobjekt:

1.  Erstellen Sie eine [**FORMATETC-Struktur.**](/windows/win32/api/objidl/ns-objidl-formatetc) Legen Sie den **cfFormat-Member** auf den entsprechenden Zwischenablageformatwert und den **gebundenen** Member auf TYMED \_ CABLOBAL fest.
2.  Erstellen Sie eine [**STGMEDIUM-Struktur.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Legen Sie den **tymed-Member** auf TYMED \_ CABLOBAL fest.
3.  Erstellen Sie ein globales Speicherobjekt, indem Sie [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) aufrufen, um einen Speicherblock mit entsprechender Größe zuzuordnen.
4.  Weisen Sie den Datenblock zu, der an die von [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)zurückgegebene Adresse übertragen werden soll.
5.  Weisen Sie die Adresse des globalen Speicherobjekts dem **hGlobal-Member** der [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) zu.
6.  Laden Sie das Format in das Datenobjekt, indem [**Sie IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufrufen und die in den vorherigen Schritten erstellten [**FORMATETC-**](/windows/win32/api/objidl/ns-objidl-formatetc) und [**STGMEDIUM-Strukturen**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) übergeben.

Die folgende Beispielfunktion erstellt ein globales Speicherobjekt, das einen **DWORD-Wert** enthält, und lädt es in ein Datenobjekt. Der **pdtobj-Parameter** ist ein Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts, **cf** ist der Zwischenablageformatwert, und **dw** ist der Datenwert.


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>Implementieren von IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ist die primäre Schnittstelle eines Datenobjekts. Sie muss von allen Datenobjekten implementiert werden. Sie wird sowohl von der Quelle als auch vom Ziel für eine Vielzahl von Zwecken verwendet, einschließlich:

-   Laden von Daten in das Datenobjekt.
-   Extrahieren von Daten aus dem Datenobjekt.
-   Bestimmen der Datentypen im Datenobjekt.
-   Bereitstellen von Feedback zum Ergebnis der Datenübertragung an das Datenobjekt.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) unterstützt eine Reihe von Methoden. In diesem Abschnitt wird erläutert, wie die drei wichtigsten Methoden für Shell-Datenobjekte, [SetData,](#setdata-method) [EnumFormatEtc](#enumformatetc-method)und [GetData,](#getdata-method)implementiert werden. Eine Erläuterung der anderen Methoden finden Sie in der **IDataObject-Referenz.**

### <a name="setdata-method"></a>SetData-Methode

Die primäre Funktion der [**IDataObject::SetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) besteht darin, der Quelle das Laden von Daten in das Datenobjekt zu ermöglichen. Für jedes einzubindbare Format erstellt die Quelle eine [**FORMATETC-Struktur,**](/windows/win32/api/objidl/ns-objidl-formatetc) um das Format zu identifizieren, und eine [**STGMEDIUM-Struktur,**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) die einen Zeiger auf die Daten enthält. Die Quelle ruft dann die **IDataObject::SetData-Methode** des Objekts auf und übergibt die **FORMATETC-** und **STGMEDIUM-Strukturen** des Formats. Die -Methode muss diese Informationen speichern, damit sie verfügbar sind, wenn das Ziel [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufruft, um Daten aus dem -Objekt zu extrahieren.

Beim Übertragen von Dateien fügt die Shell jedoch häufig die Informationen für jede zu übertragende Datei in ein separates [CFSTR \_ FILECONTENTS-Format](clipboard.md) ein. Um die verschiedenen Dateien zu unterscheiden, wird der **lIndex-Member** der [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) jeder Datei auf einen Indexwert festgelegt, der die jeweilige Datei identifiziert. Ihre [**IDataObject::SetData-Implementierung**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) muss mehrere CFSTR \_ FILECONTENTS-Formate speichern können, die sich nur durch ihre **lIndex-Member** unterscheiden.

While the cursor is over the target window, the target can use the [drag-and-drop helper object](#using-the-drag-and-drop-helper-object) to specify the drag image. The drag-and-drop helper object calls [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) to load private formats into the data object that are used for cross-process support. To support the drag-and-drop helper object, your **IDataObject::SetData** implementation must be able to accept and store arbitrary private formats.

Nachdem die Daten gelöscht wurden, erfordern einige Arten der Shell-Datenübertragung, dass das Ziel [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufruft, um dem Datenobjekt Informationen zum Ergebnis des Ablagevorgangs bereitzustellen. Wenn Beispielsweise Dateien mit einem optimierten Verschiebevorgang verschoben werden, löscht das Ziel normalerweise die ursprünglichen Dateien, dies ist jedoch nicht erforderlich. Das Ziel informiert das Datenobjekt darüber, ob es die Dateien gelöscht hat, indem **es IDataObject::SetData** mit einem [CFSTR \_ LOGICALPERFORMEDDROPEFFECT-Format](clipboard.md) aufruft. Es gibt mehrere andere [Shell-Zwischenablageformate,](clipboard.md) die auch vom Ziel verwendet werden, um Informationen an das Datenobjekt zu übergeben. Ihre **IDataObject::SetData-Implementierung** muss in der Lage sein, diese Formate zu erkennen und entsprechend zu reagieren. Weitere Informationen finden Sie unter [Behandeln von Shell-Datenübertragungsszenarien.](datascenarios.md)

### <a name="enumformatetc-method"></a>EnumFormatEtc-Methode

Wenn das Ziel ein Datenobjekt empfängt, ruft es häufig [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) auf, um zu bestimmen, welche Formate das Objekt enthält. Die -Methode erstellt ein OLE-Enumerationsobjekt und gibt einen Zeiger auf die [**IEnumFORMATETC-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) des Objekts zurück. Das Ziel verwendet dann die -Schnittstelle, um die verfügbaren Formate aufzuzählen.

Ein Enumerationsobjekt sollte immer die verfügbaren Formate in der Reihenfolge ihrer Qualität aufzählen, beginnend mit der besten. Die relative Qualität der Formate wird durch die Ablagequelle definiert. Im Allgemeinen enthalten die Formate mit der höchsten Qualität die umfassendsten und vollständigsten Daten. Beispielsweise würde ein 24-Bit-Farbbild normalerweise als eine höhere Qualität angesehen als eine graue Version dieses Bilds. Der Grund für das Aufzählen von Formaten in der Reihenfolge ihrer Qualität ist, dass Ziele in der Regel aufzählen, bis sie zu einem von ihnen unterstützten Format gelangen und dann dieses Format verwenden, um die Daten zu extrahieren. Damit dieses Verfahren das beste verfügbare Format erzeugt, das das Ziel unterstützen kann, müssen die Formate in der Reihenfolge ihrer Qualität aufzählt werden.

Ein Enumerationsobjekt für Shell-Daten wird auf die gleiche Weise wie bei anderen Arten der Datenübertragung implementiert, mit einer wichtigen Ausnahme. Da Datenobjekte in der Regel nur ein Datenelement pro Format enthalten, werden normalerweise alle Formate aufzählt, die an [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)übergeben werden. Wie im Abschnitt [SetData-Methode](#setdata-method) erläutert, können Shell-Datenobjekte jedoch mehrere [CFSTR \_ FILECONTENTS-Formate](clipboard.md) enthalten.

Da der Zweck von [**IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) darin besteht, dem Ziel zu ermöglichen, zu bestimmen, welche Datentypen vorhanden sind, ist es nicht erforderlich, mehr als ein [CFSTR \_ FILECONTENTS-Format](clipboard.md) aufzuzählen. Wenn das Ziel wissen muss, wie viele dieser Formate das Datenobjekt enthält, kann das Ziel diese Informationen aus dem zugehörigen CFSTR \_ FILEDESCRIPTOR-Format abrufen. Weitere Informationen zum Implementieren von **IDataObject::EnumFormatEtc** finden Sie in der Referenzdokumentation der Methode.

### <a name="getdata-method"></a>GetData-Methode

Das Ziel ruft [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) auf, um ein bestimmtes Datenformat zu extrahieren. Das Ziel gibt das Format an, indem die entsprechende [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) übergeben wird. **IDataObject::GetData** gibt die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) des Formats zurück.

Das Ziel kann den **gebundenen** Member der [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) auf einen bestimmten TYMED \_ *XXX-Wert* festlegen, um anzugeben, welcher Datenübertragungsmechanismus zum Extrahieren der Daten verwendet wird. Das Ziel kann jedoch auch eine allgemeinere Anforderung erstellen und das Datenobjekt entscheiden lassen. Um das Datenobjekt aufzufordern, den Datenübertragungsmechanismus auszuwählen, legt das Ziel alle TYMED \_ *XXX-Werte* fest, die es unterstützt. [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) wählt einen dieser Datenübertragungsmechanismen aus und gibt die entsprechende [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) zurück. Tymed  wird beispielsweise häufig auf TYMED \_ MILLLOBAL \| TYMED \_ ISTREAM \| TYMED \_ ISTORAGE festgelegt, um einen der drei Shell-Datenübertragungsmechanismen anzufordern.

> [!Note]  
> Da es mehrere [CFSTR \_ FILECONTENTS-Formate](clipboard.md) geben kann, reichen die **cfFormat-** und **tymed-Member** der [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) nicht aus, um anzugeben, welche [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) zurückgeben soll. Für das CFSTR \_ FILECONTENTS-Format muss **IDataObject::GetData** auch den **lIndex-Member** der **FORMATETC-Struktur** untersuchen, um die richtige **STGMEDIUM-Struktur** zurückzugeben.

 

The [CFSTR\_INDRAGLOOP](clipboard.md) format is placed in data objects to allow targets to check the status of the drag-and-drop loop while avoiding memory intensive rendering of the object's data. Die Daten des Formats sind ein **DWORD-Wert,** der auf einen Wert ungleich 0 (null) festgelegt wird, wenn sich das Datenobjekt in einer Ziehschleife befindet. Der Datenwert des Formats wird auf 0 (null) festgelegt, wenn die Daten gelöscht wurden. Wenn ein Ziel dieses Format anfordert und nicht von der Quelle geladen wurde, sollte [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) so reagieren, als ob die Quelle das Format mit dem Wert 0 (null) geladen hätte.

While the cursor is over the target window, the target can use the [drag-and-drop helper object](#using-the-drag-and-drop-helper-object) to specify the drag image. The drag-and-drop helper object calls [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) to load private formats into the data object that are used for cross-process support. Später wird [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufgerufen, um sie abzurufen. Um das Drag & Drop-Hilfsobjekt zu unterstützen, muss die Implementierung des Shelldatenobjekts in der Lage sein, beliebige private Formate zurückzugeben, wenn sie angefordert werden.

### <a name="implementing-idropsource"></a>Implementieren von IDropSource

Die Quelle muss ein Objekt erstellen, das eine [**IDropSource-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idropsource) verfügbar macht. This interface allows the source to update the *drag image* that indicates the current position of the cursor and to provide feedback to the system on how to terminate a drag-and-drop operation. **IDropSource** verfügt über zwei Methoden: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) und [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback-Methode

In der Ziehschleife ist eine Ablagequelle dafür verantwortlich, die Cursorposition nachzuverfolgen und ein entsprechendes Ziehbild anzuzeigen. In einigen Fällen können Sie jedoch die Darstellung des Ziehbilds ändern, wenn es sich über dem Fenster des Ablageziels befindet.

Wenn der Cursor das Zielfenster ein- oder verlässt und sich über das Zielfenster bewegt, ruft das System in regelmäßigen Abständen die [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) des Ziels auf. Das Ziel antwortet mit einem [**DROPEFFECT-Wert,**](../com/dropeffect-constants.md) der über die [**GiveFeedback-Methode**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) an die Quelle weitergeleitet wird. Bei Bedarf kann die Quelle die Darstellung des Cursors basierend auf dem **DROPEFFECT-Wert** ändern. Weitere Informationen finden Sie in den Verweisen auf **GiveFeedback** und [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

### <a name="querycontinuedrag-method"></a>QueryContinueDrag-Methode

Diese Methode wird aufgerufen, wenn sich die Maustaste oder der Tastaturzustand ändert, während sich das Datenobjekt in der Ziehschleife befindet. Er benachrichtigt die Quelle, ob die ESC-Taste gedrückt wurde, und stellt den aktuellen Zustand der Tastenkombinationen bereit, z. B. STRG oder UMSCHALT. Der Rückgabewert der [**QueryContinueDrag-Methode**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) gibt eine von drei Aktionen an:

-   S \_ OK. Fortsetzen des Ziehvorgangs
-   DRAGDROP \_ S \_ DROP. Löschen Sie die Daten. Das System ruft dann die [**IDropTarget::D rop-Methode**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) des Ziels auf.
-   DRAGDROP \_ S \_ CANCEL. Beenden Sie die Ziehschleife, ohne die Daten zu löschen. Dieser Wert wird normalerweise zurückgegeben, wenn die ESCAPE-Taste gedrückt wurde.

Weitere Informationen finden Sie in den Verweisen [**queryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) und [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

## <a name="how-a-target-handles-a-data-object"></a>So behandelt ein Ziel ein Datenobjekt

Das Ziel empfängt ein Datenobjekt, wenn es entweder das Datenobjekt aus der Zwischenablage abruft oder vom Benutzer im Zielfenster abgelegt wird. Das Ziel kann dann Daten aus dem Datenobjekt extrahieren. Bei Bedarf kann das Ziel auch das Datenobjekt über das Ergebnis des Vorgangs benachrichtigen. Vor einer Shell-Datenübertragung muss sich ein Ablageziel auf den Vorgang vorbereiten:

1.  Das Ziel muss [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) aufrufen, um einen gültigen Zwischenablageformatwert für alle Shellformate außer [CF \_ HDROP](clipboard.md)abzurufen, die möglicherweise im Datenobjekt enthalten sind. CF \_ HDROP ist bereits ein gültiges Zwischenablageformat und muss nicht registriert werden.
2.  To support a drag-and-drop operation, the target must implement an [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface and register a target window. Um ein Zielfenster zu registrieren, ruft das Ziel [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) auf und übergibt das Handle des Fensters und den **IDropTarget-Schnittstellenzeiger.**

Bei Übertragungen in der Zwischenablage erhält das Ziel keine Benachrichtigung, dass ein Datenobjekt in der Zwischenablage platziert wurde. In der Regel wird eine Anwendung durch eine Benutzeraktion benachrichtigt, dass sich ein Objekt in der Zwischenablage befindet, z. B. durch Klicken auf die Schaltfläche Einfügen auf der Symbolleiste der Anwendung. Das Ziel ruft dann den [**IDataObject-Zeiger**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts aus der Zwischenablage ab, indem [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)aufgerufen wird. For drag-and-drop data transfers, the system uses the target's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface to provide the target with information about the progress of the data transfer:

-   Das System ruft [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) auf, wenn der Cursor in das Zielfenster eintritt.
-   Das System ruft [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) regelmäßig auf, wenn der Cursor über das Zielfenster geht, um dem Ziel die aktuelle Cursorposition zuzuweisen.
-   Das System ruft [**IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) auf, wenn der Cursor das Zielfenster verlässt.
-   Das System ruft [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) auf, wenn der Benutzer das Datenobjekt im Zielfenster löscht.

Eine Erläuterung der Implementierung dieser Methoden finden Sie unter [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Wenn die Daten gelöscht werden, stellt [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) dem Ziel einen Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts bereit. Das Ziel verwendet dann diese Schnittstelle, um Daten aus dem Datenobjekt zu extrahieren.

### <a name="extracting-shell-data-from-a-data-object"></a>Extrahieren von Shelldaten aus einem Datenobjekt

Nachdem ein Datenobjekt gelöscht oder aus der Zwischenablage abgerufen wurde, kann das Ziel die benötigten Daten extrahieren. Der erste Schritt im Extraktionsprozess besteht in der Regel darin, die im Datenobjekt enthaltenen Formate aufzuzählen:

-   Rufen Sie [**IDataObject::EnumFormatEtc auf.**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) Das Datenobjekt erstellt ein OLE-Standardenumerationsobjekt und gibt einen Zeiger auf seine [**IEnumFORMATETC-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) zurück.
-   Verwenden Sie die [**IEnumFORMATETC-Methoden,**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) um die im Datenobjekt enthaltenen Formate aufzuzählen. Dieser Vorgang ruft in der Regel eine [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) für jedes Format ab, das das -Objekt enthält. Das Enumerationsobjekt gibt jedoch normalerweise nur eine einzelne **FORMATETC-Struktur** für das [CFSTR \_ FILECONTENTS-Format](clipboard.md) zurück, unabhängig davon, wie viele formate im Datenobjekt enthalten sind.
-   Wählen Sie ein oder mehrere Formate aus, die extrahiert werden sollen, und speichern Sie deren [**FORMATETC-Strukturen.**](/windows/win32/api/objidl/ns-objidl-formatetc)

Um ein bestimmtes Format abzurufen, übergeben Sie die zugeordnete [**FORMATETC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) an [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Diese Methode gibt eine [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) zurück, die Zugriff auf die Daten bereitstellt. Um einen bestimmten Datenübertragungsmechanismus anzugeben, legen Sie den **gebundenen** Wert der **FORMATETC-Struktur** auf den entsprechenden TYMED \_ *XXX-Wert* fest. Um das Datenobjekt aufzufordern, einen Datenübertragungsmechanismus auszuwählen, legt das Ziel die TYMED \_ *XXX-Werte* für jeden Datenübertragungsmechanismus fest, den das Ziel verarbeiten kann. Das Datenobjekt wählt einen dieser Datenübertragungsmechanismen aus und gibt die entsprechende **STGMEDIUM-Struktur** zurück.

Bei den meisten Formaten kann das Ziel die Daten abrufen, indem es die [**FORMATTC-Struktur**](/windows/win32/api/objidl/ns-objidl-formatetc) übergibt, die es beim Aufzählen der verfügbaren Formate erhalten hat. Eine Ausnahme von dieser Regel ist [CFSTR \_ FILECONTENTS.](clipboard.md) Da ein Datenobjekt mehrere Instanzen dieses Formats enthalten kann, entspricht die vom Enumerator zurückgegebene **FORMATETC-Struktur** möglicherweise nicht dem formatspezifischen Format, das Sie extrahieren möchten. Zusätzlich zum Angeben der **Member cfFormat** und **tymed** müssen Sie auch den **lIndex-Member** auf den Indexwert der Datei festlegen. Weitere Informationen finden Sie im Abschnitt *Using the CFSTR FILECONTENTS Format to Extract Data from a File (Verwenden des CFSTR \_ FILECONTENTS-Formats zum Extrahieren von Daten aus einer Datei)* unter Handling Shell Data Transfer Scenarios (Behandeln von [Shell-Datenübertragungsszenarien).](datascenarios.md)

Der Datenextraktionsvorgang hängt vom Typ des Zeigers ab, der in der zurückgegebenen [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) enthalten ist. Wenn die -Struktur einen Zeiger auf eine [**IStream-**](/windows/win32/api/objidl/nn-objidl-istream) oder [**IStorage-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-istorage) enthält, verwenden Sie die Schnittstellenmethoden, um die Daten zu extrahieren. Der Prozess des Extrahierens von Daten aus einem globalen Speicherobjekt wird im nächsten Abschnitt erläutert.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extrahieren eines globalen Speicherobjekts aus einem Datenobjekt

Viele der Shell-Datenformate haben die Form eines globalen Speicherobjekts. Verwenden Sie das folgende Verfahren, um ein Format zu extrahieren, das ein globales Speicherobjekt aus einem Datenobjekt enthält, und weisen Sie dessen Daten einer lokalen Variablen zu:

1.  Erstellen Sie eine [**FORMATETC-Struktur.**](/windows/win32/api/objidl/ns-objidl-formatetc) Legen Sie den **cfFormat-Member** auf den entsprechenden Zwischenablageformatwert und den **gebundenen** Member auf TYMED \_ CABLOBAL fest.
2.  Erstellen Sie eine leere [**STGMEDIUM-Struktur.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
3.  Rufen Sie [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)auf, und übergeben Sie Zeiger auf die [**Formatetc-**](/windows/win32/api/objidl/ns-objidl-formatetc) und [**STGMEDIUM-Strukturen.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

    Wenn [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) zurückgegeben wird, enthält die [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) einen Zeiger auf das globale Speicherobjekt, das die Daten enthält.

4.  Weisen Sie die Daten einer lokalen Variablen zu, indem [**Sie GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) aufrufen und den **hGlobal-Member** der [**STGMEDIUM-Struktur**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) übergeben.
5.  Rufen Sie [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) auf, um die Sperre für das globale Speicherobjekt freizugeben.
6.  Rufen Sie [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) auf, um das globale Speicherobjekt freizugeben.

> [!Note]  
> Sie müssen [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) verwenden, um das globale Speicherobjekt freizugeben, nicht [**GlobalFree.**](/windows/win32/api/winbase/nf-winbase-globalfree)

 

Das folgende Beispiel zeigt, wie ein **DWORD-Wert** extrahiert wird, der als globales Speicherobjekt aus einem Datenobjekt gespeichert ist. Der **pdtobj-Parameter** ist ein Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts, **cf** ist das Zwischenablageformat, das die gewünschten Daten identifiziert, und **pdwOut** wird verwendet, um den Datenwert zurückzugeben.


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>Implementieren von IDropTarget

Das System verwendet die [**IDropTarget-Schnittstelle,**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) um mit dem Ziel zu kommunizieren, während sich der Cursor über dem Zielfenster befindet. Die Antworten des Ziels werden über die [**IDropSource-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idropsource) an die Quelle weitergeleitet. Abhängig von der Antwort kann die Quelle das Symbol ändern, das die Daten darstellt. If the drop target needs to specify the data icon, it can do so by creating a [drag-and-drop helper object](#using-the-drag-and-drop-helper-object).

With conventional drag-and-drop operations, the target informs the data object of the outcome of the operation by setting the *pdwEffect* parameter of [**IDropTarget::Drop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) to the appropriate [**DROPEFFECT**](../com/dropeffect-constants.md) value. Bei Shell-Datenobjekten muss das Ziel möglicherweise auch [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)aufrufen. Eine Erläuterung, wie Ziele auf verschiedene Datenübertragungsszenarien reagieren sollten, finden Sie unter [Behandeln von Shell-Datenübertragungsszenarien.](datascenarios.md)

In den folgenden Abschnitten wird kurz erläutert, wie die Methoden [**IDropTarget::D ragEnter,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)und [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) implementiert werden. Weitere Informationen finden Sie in der Referenzdokumentation.

### <a name="dragenter-method"></a>DragEnter-Methode

Das System ruft die [**IDropTarget::D ragEnter-Methode**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) auf, wenn der Cursor in das Zielfenster eintritt. Seine Parameter stellen dem Ziel die Position des Cursors, den Zustand von Tastaturmodifizierertasten wie strg und einen Zeiger auf die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts bereit. Das Ziel ist für die Verwendung dieser Schnittstelle verantwortlich, um zu bestimmen, ob es eines der im Datenobjekt enthaltenen Formate akzeptieren kann. Wenn dies dere ist, bleibt der Wert von *pdwEffect* normalerweise unverändert. Wenn keine Daten aus dem Datenobjekt akzeptiert werden können, wird der *pdwEffect-Parameter* auf DROPEFFECT \_ NONE festgelegt. Das System übergibt den Wert dieses Parameters an die [**IDropSource-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idropsource) des Datenobjekts, damit das entsprechende Ziehbild angezeigt werden kann.

Ziele sollten die [**IDataObject::GetData-Methode**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) nicht verwenden, um Shelldaten zu rendern, bevor sie gelöscht wurden. Das vollständige Rendern der Objektdaten für jedes solche Vorkommen kann dazu führen, dass der Ziehcursor angehalten wird. Um dieses Problem zu vermeiden, enthalten einige Shell-Objekte ein [CFSTR \_ INDRAGLOOP-Format.](clipboard.md) Durch Extrahieren dieses Formats können Ziele den Status der Ziehschleife überprüfen und gleichzeitig das speicherintensive Rendern der Daten des Objekts vermeiden. Der Datenwert des Formats ist ein **DWORD,** das auf einen Wert ungleich 0 (null) festgelegt wird, wenn sich das Datenobjekt in einer Ziehschleife befindet. Der Datenwert des Formats wird auf 0 (null) festgelegt, wenn die Daten gelöscht wurden.

Wenn das Ziel Daten aus dem Datenobjekt akzeptieren kann, sollte **grfKeyState** untersucht werden, um zu bestimmen, ob Modifizierertasten gedrückt wurden, um das normale Ablageverhalten zu ändern. Beispielsweise ist der Standardvorgang in der Regel eine Verschiebung, aber das Drücken der STRG-Taste weist in der Regel auf einen Kopiervorgang hin.

While the cursor is over the target window, the target can use the [drag-and-drop helper object](#using-the-drag-and-drop-helper-object) to replace the data object's drag image with its own. If so, [**IDropTarget::DragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) should call [**IDropTargetHelper::DragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) to pass the information contained in the *DragEnter* parameters to the drag-and-drop helper object.

### <a name="dragover-method"></a>DragOver-Methode

Während sich der Cursor innerhalb des Zielfensters bewegt, ruft das System regelmäßig die [**IDropTarget::D ragOver-Methode**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) auf. Die Parameter geben dem Ziel die Position des Cursors und den Status der Tastaturmodifizierertasten, z. B. die STRG-TASTE, an. **IDropTarget::D ragOver** hat die gleichen Aufgaben wie [**IDropTarget::D ragEnter,**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)und die Implementierungen sind in der Regel sehr ähnlich.

If the target is using the drag-and-drop helper object, [**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) should call [**IDropTargetHelper::DragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) to forward the information contained in the *DragOver* parameters to the drag-and-drop helper object.

### <a name="drop-method"></a>Drop-Methode

Das System ruft die [**IDropTarget::D rop-Methode**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) auf, um das Ziel zu benachrichtigen, dass der Benutzer die Daten gelöscht hat, in der Regel durch Loslassen der Maustaste. **IDropTarget::D rop** verfügt über die gleichen Parameter wie [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). Das Ziel antwortet normalerweise durch Extrahieren eines oder mehrerer Formate aus dem Datenobjekt. Nach Abschluss des Vorgangs sollte das Ziel den *parameter pdwEffect* auf einen [**DROPEFFECT-Wert**](../com/dropeffect-constants.md) festlegen, der das Ergebnis des Vorgangs angibt. Bei einigen Arten von Shell-Datenübertragungen muss das Ziel auch [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufrufen, um ein Format mit zusätzlichen Informationen zum Ergebnis des Vorgangs an das Datenobjekt zu übergeben. Eine ausführliche Erläuterung finden Sie unter [Behandeln von Shell-Datenübertragungsszenarien.](datascenarios.md)

If the target is using the drag-and-drop helper object, [**IDropTarget::Drop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) should call [**IDropTargetHelper::Drop**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) to forward the information contained in the [**IDropTargetHelper::DragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) parameters to the drag-and-drop helper object.

## <a name="using-the-drag-and-drop-helper-object"></a>Verwenden des Drag & Drop-Hilfsobjekts

The drag-and-drop helper object (CLSID\_DragDropHelper) is exported by the Shell to allow targets to specify the drag image while it is over the target window. To use the drag-and-drop helper object, create an in-process server object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with a class identifier (CLSID) of CLSID\_DragDropHelper. Das Drag & Drop-Hilfsobjekt macht zwei Schnittstellen verfügbar, die auf folgende Weise verwendet werden:

-   Die [**IDragSourceHelper-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) ermöglicht es dem Ablageziel, ein Symbol anzugeben, das das Datenobjekt darstellt.
-   The [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) interface allows the drop target to inform the drag-and-drop helper object of the cursor location, and to show or hide the data icon.

### <a name="using-the-idragsourcehelper-interface"></a>Verwenden der IDragSourceHelper-Schnittstelle

The [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) interface is exposed by the drag-and-drop helper object to allow a drop target to provide the image that will be displayed while the cursor is over the target window. **IDragSourceHelper** bietet zwei alternative Möglichkeiten, die Bitmap anzugeben, die als Ziehbild verwendet werden soll:

-   Drop targets that have a window can register a DI\_GETDRAGIMAGE window message for it by initializing the drag-and-drop helper object with [**IDragSourceHelper::InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Wenn das Ziel eine DI \_ GETDRAGIMAGE-Nachricht empfängt, fügt der Handler die Bitmapinformationen des Ziehbilds in die [**SHDRAGIMAGE-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) ein, die als *lParam-Wert* der Nachricht übergeben wird.
-   Windowless drop targets specify a bitmap when they initialize the drag-and-drop helper object with [**IDragSourceHelper::InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Verwenden der IDropTargetHelper-Schnittstelle

Diese Schnittstelle ermöglicht es dem Ablageziel, das Drag & Drop-Hilfsobjekt zu benachrichtigen, wenn der Cursor das Ziel erreicht oder verlässt. While the cursor is over the target window, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) allows the target to give the drag-and-drop helper object the information that the target receives through its [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.

Vier der [**IDropTargetHelper-Methoden**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) –[**IDropTargetHelper::D ragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D ragLeave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)und [**IDropTargetHelper::D rop**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)– sind der [**IDropTarget-Methode**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) mit dem gleichen Namen zugeordnet. To use the drag-and-drop helper object, each of the **IDropTarget** methods should call the corresponding **IDropTargetHelper** method to forward the information to the drag-and-drop helper object. The fifth **IDropTargetHelper** method, [**IDropTargetHelper::Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), notifies the drag-and-drop helper object to show or hide the drag image. Diese Methode wird beim Ziehen über ein Zielfenster in einem Videomodus mit niedriger Farbtiefe verwendet. Es ermöglicht dem Ziel, das Ziehbild auszublenden, während es das Fenster zeichnet.

 

 
