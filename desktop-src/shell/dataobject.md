---
description: Das Datenobjekt ist für alle shelldatenübertragungen von zentraler Bedeutung.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Shelldatenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812e5c18f5a2120fbf22682c6e768dc005128630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214432"
---
# <a name="shell-data-object"></a>Shelldatenobjekt

Das Datenobjekt ist für alle shelldatenübertragungen von zentraler Bedeutung. Dabei handelt es sich hauptsächlich um einen Container zum Speichern der übertragenen Daten. Das Ziel kann jedoch auch mit dem Datenobjekt kommunizieren, um einige spezielle Arten von shelldatenübertragungen, wie z. b. optimierte Verschiebungen, zu vereinfachen. Dieses Thema enthält eine allgemeine Erörterung der Funktionsweise von shelldatenobjekten, der Art und Weise, wie Sie von einer Quelle erstellt werden und wie Sie von einem Ziel behandelt werden. Ausführliche Informationen zur Verwendung von Datenobjekten für die Übertragung unterschiedlicher Arten von shelldaten finden Sie unter [Handling Shell Datenübertragung Szenarios](datascenarios.md).

-   [Funktionsweise von Datenobjekten](#how-data-objects-work)
    -   [Zwischenablage Formate](#clipboard-formats)
    -   [FORMATETC-Struktur](#formatetc-structure)
    -   [STGMEDIUM-Struktur](#stgmedium-structure)
-   [So erstellt eine Quelle ein Datenobjekt](#how-a-source-creates-a-data-object)
    -   [Vorgehensweise beim Hinzufügen eines globalen Speicher Objekts zu einem Datenobjekt](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementieren von IDataObject](#implementing-idataobject)
    -   [Implementieren von IDropSource](#implementing-idropsource)
-   [Verarbeiten eines Datenobjekts durch ein Ziel](#how-a-target-handles-a-data-object)
    -   [Extrahieren von shelldaten aus einem Datenobjekt](#extracting-shell-data-from-a-data-object)
    -   [Implementieren von IDropTarget](#implementing-idroptarget)
-   [Verwenden des Drag & amp; Drop-Hilfsobjekts](#using-the-drag-and-drop-helper-object)
    -   [Verwenden der idragsourcehelper-Schnittstelle](#using-the-idragsourcehelper-interface)
    -   [Verwenden der idroptargethelper-Schnittstelle](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Funktionsweise von Datenobjekten

Datenobjekte sind Component Object Model (com)-Objekte, die von der Datenquelle zum Übertragen von Daten an ein Ziel erstellt werden. Sie enthalten in der Regel mehr als ein Datenelement. Hierfür gibt es zwei Gründe:

-   Obwohl fast jeder Datentyp mit einem Datenobjekt übertragen werden kann, weiß die Quelle in der Regel nicht, welche Art von Daten das Ziel annehmen kann. Beispielsweise kann es sich bei den Daten um einen Teil eines formatierten Textdokuments handeln. Obwohl das Ziel möglicherweise in der Lage ist, komplexe Formatierungsinformationen zu verarbeiten, kann es möglicherweise auch nur ANSI-Text akzeptieren. Aus diesem Grund enthalten Datenobjekte häufig dieselben Daten in verschiedenen Formaten. Das Ziel kann dann die Daten in einem Format extrahieren, das Sie verarbeiten kann.
-   Datenobjekte können auch zusätzliche Datenelemente enthalten, bei denen es sich nicht um Versionen der Quelldaten handelt. Diese Art von Datenelement stellt in der Regel zusätzliche Informationen zum Datenübertragungs Vorgang bereit. Beispielsweise verwendet die Shell zusätzliche Datenelemente, um anzugeben, ob eine Datei kopiert oder verschoben werden soll.

### <a name="clipboard-formats"></a>Zwischenablage Formate

Jedes Datenelement in einem Datenobjekt weist ein zugeordnetes Format auf, das in der Regel als *Zwischenablage Format* bezeichnet wird. Es gibt eine Reihe von Standardformaten in der Zwischenablage, die in winuser. h deklariert sind und den häufig verwendeten Datentypen entsprechen. Zwischenablage Formate sind ganze Zahlen, aber Sie werden normalerweise durch Ihren äquivalenten Namen bezeichnet, der die Form CF \_ *xxx* hat. Beispielsweise ist das Zwischenablage Format für ANSI-Text CF- \_ Text.

Anwendungen können den Bereich der verfügbaren Zwischenablage Formate erweitern, indem Sie private Formate definieren. Zum Definieren eines privaten Formats Ruft eine Anwendung [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) mit einer Zeichenfolge auf, die das Format angibt. Die von der Funktion zurückgegebene Ganzzahl ohne Vorzeichen ist ein gültiger Format Wert, der genau wie ein Standardmäßiges Zwischenablage Format verwendet werden kann. Allerdings müssen sowohl Quelle als auch Ziel das Format registrieren, damit es verwendet werden kann. Mit einer Ausnahme –[CF \_ HDROP](clipboard.md)– werden die Zwischenablage Formate, die zum Übertragen von shelldaten verwendet werden, als private Formate definiert. Sie müssen von der Quelle und dem Ziel registriert werden, bevor Sie verwendet werden können. Eine Beschreibung der verfügbaren shellzwischenablage Formate finden Sie unter shellzwischenablage Formate.

Obwohl es einige Ausnahmen gibt, enthalten Datenobjekte normalerweise nur ein Datenelement für jedes Zwischenablage Format, das Sie unterstützen. Diese eins-zu-Eins-Korrelation zwischen Format und Daten ermöglicht die Verwendung des Format Werts als Bezeichner für das zugeordnete Datenelement. Tatsächlich wird bei der Erörterung der Inhalte eines Datenobjekts ein bestimmtes Datenelement in der Regel als "Format" bezeichnet, und es wird durch den Format Namen verwiesen. Beispielsweise Ausdrücke, z. b. "Extrahieren des CF- \_ Text Formats..." werden in der Regel verwendet, wenn das ANSI-Text Datenelement eines Datenobjekts diskutiert wird.

Wenn das Ablage Ziel den Zeiger auf das Datenobjekt empfängt, listet das Ablage Ziel die verfügbaren Formate auf, um zu bestimmen, welche Arten von Daten verfügbar sind. Anschließend wird mindestens eines der verfügbaren Formate angefordert, und die Daten werden extrahiert. Die spezifische Methode, mit der das Ziel shelldaten aus einem Datenobjekt extrahiert, variiert im Format. Dies wird ausführlich erläutert, [wie ein Ziel ein Datenobjekt behandelt](#how-a-target-handles-a-data-object).

Bei einfachen Datenübertragungen zwischen der Zwischenablage werden die Daten in einem globalen Speicher Objekt platziert. Die Adresse des Objekts wird zusammen mit dem Format in der Zwischenablage platziert. Das Format der Zwischenablage teilt dem Ziel mit, welche Art von Daten bei der zugeordneten Adresse gefunden werden. Während einfache Zwischenablage Übertragungen leicht implementiert werden können:

-   Datenobjekte stellen eine viel flexiblere Methode zum Übertragen von Daten dar.
-   Datenobjekte eignen sich besser für die Übertragung großer Datenmengen.
-   Datenobjekte müssen verwendet werden, um Daten mit einem Drag & Drop-Vorgang zu übertragen.

Aus diesen Gründen werden von allen shelldatenübertragungen Datenobjekte verwendet. Bei Datenobjekten werden Zwischenablage Formate nicht direkt verwendet. Stattdessen werden Datenelemente mit einer Generalisierung des Zwischenablage Formats, einer [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur, identifiziert.

### <a name="formatetc-structure"></a>FORMATETC-Struktur

Die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur ist eine erweiterte Version eines Zwischenablage Formats. Wie bei shelldatenübertragungen verwendet, hat die **FORMATETC** -Struktur die folgenden Eigenschaften:

-   Ein Datenelement wird weiterhin durch das Zwischenablage Format im **cfFormat** -Member identifiziert.
-   Die Datenübertragung ist nicht auf globale Speicher Objekte beschränkt. Der **TYMED** -Member wird verwendet, um den Datenübertragungsmechanismus anzugeben, der in der zugeordneten [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur enthalten ist. Sie wird auf einen der Werte vom [**typmed \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) festgelegt.
-   Die Shell verwendet das **Lindex** -Element mit dem [cfstr \_ File Contents](clipboard.md) -Format, damit ein Datenobjekt mehr als ein Datenelement Pro Format enthalten kann. Eine Erläuterung zur Verwendung dieses Formats finden Sie im Abschnitt *Verwenden des cfstr \_ File Contents-Formats zum Extrahieren von Daten aus einer Datei* im Abschnitt [Handling Shell Datenübertragung Szenarios](datascenarios.md).
-   Der **dwAspect** -Member ist in der Regel auf DVASPECT-Inhalt festgelegt \_ . In "shlobj. h" sind jedoch drei Werte definiert, die für die Shell-Datenübertragung verwendet werden können. 

    |                     |                                                                                                   |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | DVASPECT- \_ Kopie      | Wird verwendet, um anzugeben, dass das Format eine Kopie der Daten darstellt.                                   |
    | DVASPECT- \_ Link      | Wird verwendet, um anzugeben, dass das Format eine Verknüpfung zu den Daten darstellt.                               |
    | \_dvaspektkurzname | Wird im CF- \_ HDROP-Format verwendet, um einen Dateipfad anzufordern, bei dem die Namen auf das 8,3-Format verkürzt werden. |

    

     

-   Der **ptd-** Member wird nicht für shelldatenübertragungen verwendet und wird normalerweise auf **null** festgelegt.

### <a name="stgmedium-structure"></a>STGMEDIUM-Struktur

Die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur ermöglicht den Zugriff auf die Daten, die übertragen werden. Für shelldaten werden drei Datenübertragungs Mechanismen unterstützt:

-   Ein globales Speicher Objekt.
-   Eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle.
-   Eine [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle.

Der **TYMED** -Member der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur ist ein [**TYMED \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) -Wert, der den Datenübertragungsmechanismus identifiziert. Der zweite Member ist ein Zeiger, der vom Ziel verwendet wird, um die Daten zu extrahieren. Der Zeiger kann je nach dem Wert " **TYMED** " aus einer Vielzahl von Typen bestehen. Die drei **TYMED** -Werte, die für shelldatenübertragungen verwendet werden, sind in der folgenden Tabelle zusammen mit dem entsprechenden **STGMEDIUM** -Elementnamen zusammengefasst.



| tymed-Wert     | Membername | Beschreibung                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **hGlobal** | Ein Zeiger auf ein globales Speicher Objekt. Dieser Zeigertyp wird in der Regel zum übertragen kleiner Datenmengen verwendet. Beispielsweise verwendet die Shell globale Speicher Objekte, um kurze Text Zeichenfolgen (z. b. Dateinamen oder URLs) zu übertragen.                                                                                    |
| TYMED- \_ IStream  | **pstm**    | Ein Zeiger auf eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -Schnittstelle. Dieser Zeigertyp wird für die meisten shelldatenübertragungen bevorzugt, da er relativ wenig Arbeitsspeicher im Vergleich zu "TYMED \_ HGLOBAL" erfordert. Außerdem muss der \_ Daten Übertragungsmechanismus für den TYMED-IStream die Daten nicht auf bestimmte Weise speichern. |
| typmed- \_ IStorage | **pstg**    | Ein Zeiger auf eine [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle. Das Ziel Ruft die Schnittstellen Methoden zum Extrahieren der Daten auf. Wie bei TYMED \_ IStream erfordert dieser Zeigertyp relativ wenig Arbeitsspeicher. Da der IStorage-Dienst jedoch \_ weniger flexibel ist als bei TYMED \_ IStream, wird er nicht so häufig verwendet.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>So erstellt eine Quelle ein Datenobjekt

Wenn ein Benutzer eine shelldatenübertragung initiiert, ist die Quelle dafür verantwortlich, ein Datenobjekt zu erstellen und mit Daten zu laden. Im folgenden Verfahren wird der Prozess zusammengefasst:

1.  Rufen Sie [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) auf, um einen gültigen Zwischenablage-Format Wert für jedes shellformat zu erhalten, das in das Datenobjekt eingeschlossen wird. Beachten Sie, dass [CF \_ HDROP](clipboard.md) bereits ein gültiges Zwischenablage Format ist und nicht registriert werden muss.
2.  Legen Sie die zugeordneten Daten für jedes zu übertragende Format entweder in einem globalen Speicher Objekt ab, oder erstellen Sie ein Objekt, das über eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -oder [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle Zugriff auf diese Daten bereitstellt. Die **IStream** -und **IStorage** -Schnittstellen werden mit Standard-com-Techniken erstellt. Eine Erläuterung zur Handhabung von globalen Speicher Objekten finden Sie unter [Hinzufügen eines globalen Speicher Objekts zu einem Datenobjekt](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Erstellen Sie für jedes Format [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturen.
4.  Instanziieren Sie ein Datenobjekt.
5.  Laden Sie die Daten in das Datenobjekt, indem Sie die [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode für jedes unterstützte Format aufrufen und die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturen des Formats übergeben.
6.  Bei Datenübertragungen in der Zwischenablage wird [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) aufgerufen, um einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts in der Zwischenablage zu platzieren. Initiieren Sie bei Drag & Drop-Übertragungen eine *Drag-Schleife* durch Aufrufen von [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). Der **IDataObject** -Zeiger wird beim Löschen der Daten an das Ablage Ziel weitergegeben, wobei die Zieh Schleife beendet wird.

Das Datenobjekt ist nun bereit für die Übertragung an das Ziel. Bei Datenübertragungen in der Zwischenablage wird das Objekt einfach so lange aufbewahrt, bis das Ziel es durch Aufrufen von [**olegetclipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)anfordert. Bei Drag & Drop-Datenübertragungen ist das Datenobjekt dafür verantwortlich, ein Symbol zum Darstellen der Daten zu erstellen und zu verschieben, wenn der Benutzer den Cursor verschiebt. Während sich das-Objekt in der Drag-Schleife befindet, empfängt die Quelle Statusinformationen über die [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle. Weitere Informationen finden Sie unter [Implementieren von IDropSource](#implementing-idropsource).

Die Quelle empfängt keine Benachrichtigung, wenn das Datenobjekt von einem Ziel aus der Zwischenablage abgerufen wird. Wenn ein Objekt durch einen Drag & Drop-Vorgang auf einem Ziel abgelegt wird, gibt die [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) -Funktion zurück, die aufgerufen wurde, um die Drag-Schleife zu initiieren.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Vorgehensweise beim Hinzufügen eines globalen Speicher Objekts zu einem Datenobjekt

Viele der shelldatenformate sind in Form eines globalen Speicher Objekts. Verwenden Sie das folgende Verfahren, um ein Format zu erstellen, das ein globales Speicher Objekt enthält, und das Sie in das Datenobjekt laden:

1.  Erstellen Sie eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur. Legen Sie den **cfFormat** -Member auf den entsprechenden Zwischenablage Formatwert und den **TYMED** -Member auf TYMED \_ HGLOBAL fest.
2.  Erstellen Sie eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur. Legen Sie den **TYMED** -Member auf "TYMED \_ HGLOBAL" fest.
3.  Erstellen Sie ein globales Speicher Objekt, indem Sie [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) aufrufen, um einen entsprechend großen Speicherblock zuzuweisen.
4.  Weisen Sie den zu übertragenden Datenblock an die von [**globalassign**](/windows/win32/api/winbase/nf-winbase-globalalloc)zurückgegebene Adresse zu.
5.  Weisen Sie die Adresse des globalen Speicher Objekts dem **HGLOBAL** -Member der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zu.
6.  Laden Sie das Format in das Datenobjekt, indem Sie [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufrufen und die [**Formatierungs**](/windows/win32/api/objidl/ns-objidl-formatetc) -und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturen übergeben, die in den vorherigen Schritten erstellt wurden.

Mit der folgenden Beispiel Funktion wird ein globales Speicher Objekt mit einem **DWORD** -Wert erstellt und in ein Datenobjekt geladen. Der **pdtobj** -Parameter ist ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts, **CF** ist der Zwischenablage Format Wert, und **DW** ist der Datenwert.


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

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ist die primäre Schnittstelle eines Datenobjekts. Sie muss von allen Datenobjekten implementiert werden. Sie wird von Quelle und Ziel für eine Vielzahl von Zwecken verwendet, einschließlich:

-   Laden von Daten in das Datenobjekt.
-   Extrahieren von Daten aus dem Datenobjekt.
-   Die Bestimmung der Datentypen im Datenobjekt.
-   Senden von Feedback an das Datenobjekt im Rahmen der Datenübertragung.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) unterstützt eine Reihe von Methoden. In diesem Abschnitt wird erläutert, wie die drei wichtigsten Methoden für Shell-Datenobjekte, [SetData](#setdata-method), [enumformatusw](#enumformatetc-method). und [GetData](#getdata-method)implementiert werden. Eine Erläuterung der anderen Methoden finden Sie in der **IDataObject** -Referenz.

### <a name="setdata-method"></a>SetData-Methode

Die primäre Funktion der [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Methode besteht darin, dass die Quelle das Laden von Daten in das Datenobjekt zulässt. Für jedes Format, das eingeschlossen werden soll, erstellt die Quelle eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur, um das Format und eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zu identifizieren, die einen Zeiger auf die Daten enthalten soll. Die Quelle ruft dann die **IDataObject:: SetData** -Methode des Objekts auf und übergibt die **FORMATETC** -und **STGMEDIUM** -Strukturen im Format. Die-Methode muss diese Informationen speichern, damit Sie verfügbar ist, wenn das Ziel [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufruft, um Daten aus dem-Objekt zu extrahieren.

Beim Übertragen von Dateien fügt die Shell jedoch häufig die Informationen für jede Datei ein, die in ein separates [cfstr \_ File Contents](clipboard.md) -Format übertragen werden soll. Um die verschiedenen Dateien zu unterscheiden, wird der **Lindex** -Member der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur jeder Datei auf einen Indexwert festgelegt, der die jeweilige Datei identifiziert. Ihre [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) -Implementierung muss in der Lage sein, mehrere cfstr \_ File Contents-Formate zu speichern, die sich nur durch ihre **Lindex** -Member unterscheiden.

Während sich der Cursor über dem Zielfenster befindet, kann das Ziel das Drag & amp; [Drop-Hilfsobjekt](#using-the-drag-and-drop-helper-object) verwenden, um das Zieh Bild anzugeben. Das Drag & amp; Drop Helper-Objekt ruft [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) auf, um private Formate in das Datenobjekt zu laden, das für prozessübergreifende Unterstützung verwendet wird. Zur Unterstützung des Drag & Drop-Hilfsobjekts muss die **IDataObject:: SetData** -Implementierung in der Lage sein, beliebige private Formate zu akzeptieren und zu speichern.

Nachdem die Daten gelöscht wurden, erfordern einige Arten von shelldatenübertragungen, dass das Ziel [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufruft, um dem Datenobjekt Informationen zum Ergebnis des Drop-Vorgangs bereitzustellen. Wenn Sie z. b. Dateien mit einem optimierten Verschiebungs Vorgang verschieben, löscht das Ziel normalerweise die ursprünglichen Dateien, dies ist jedoch nicht zwingend erforderlich. Das Ziel informiert das Datenobjekt darüber, ob es die Dateien durch Aufrufen von **IDataObject:: SetData** mit einem [cfstr \_ logicalperformeddropeer ffect](clipboard.md) -Format gelöscht hat. Es gibt mehrere andere [shellzwischenablage Formate](clipboard.md) , die auch vom Ziel verwendet werden, um Informationen an das Datenobjekt zu übergeben. Ihre **IDataObject:: SetData** -Implementierung muss in der Lage sein, diese Formate zu erkennen und entsprechend zu reagieren. Weitere Informationen finden Sie unter [Handling Shell Datenübertragung Szenarios](datascenarios.md).

### <a name="enumformatetc-method"></a>EnumFormatEtc-Methode

Wenn das Ziel ein Datenobjekt empfängt, ruft es häufig [**formatusw**](/windows/win32/api/objidl/ns-objidl-formatetc) . auf, um zu bestimmen, welche Formate das Objekt enthält. Die-Methode erstellt ein OLE-Enumerationsobjekt und gibt einen Zeiger auf die [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) -Schnittstelle des Objekts zurück. Das Ziel verwendet dann die-Schnittstelle zum Auflisten der verfügbaren Formate.

Ein Enumerationsobjekt sollte die verfügbaren Formate immer in der Reihenfolge der Qualität auflisten, beginnend mit dem besten. Die relative Qualität von Formaten wird von der Ablage Quelle definiert. Im Allgemeinen enthalten die Formate mit der höchsten Qualität die reichsten und am meisten vollständigsten Daten. Beispielsweise würde ein 24-Bit-Farbbild normalerweise als höhere Qualität angesehen als eine Graustufen Version dieses Bilds. Der Grund für das Auflisten von Formaten in der Reihenfolge ihrer Qualität besteht darin, dass Ziele in der Regel so lange aufgelistet werden, bis Sie zu einem von Ihnen unterstützten Format gelangen. Anschließend verwenden Sie dieses Format zum Extrahieren der Daten. Damit dieses Verfahren das beste verfügbare Format erzeugt, das vom Ziel unterstützt werden kann, müssen die Formate in der Reihenfolge ihrer Qualität aufgelistet werden.

Ein Enumerationsobjekt für shelldaten wird auf die gleiche Weise wie für andere Arten der Datenübertragung implementiert, mit einer Ausnahme. Da Datenobjekte in der Regel nur ein Datenelement Pro Format enthalten, werden normalerweise alle Formate aufgelistet, die an [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)weitergegeben werden. Wie im Abschnitt [SetData-Methode](#setdata-method) erläutert, können shelldatenobjekte jedoch mehrere [cfstr \_ File Content](clipboard.md) -Formate enthalten.

Der Zweck von [**IDataObject:: enumformatusw**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) . besteht darin, das Ziel zu bestimmen, welche Datentypen vorhanden sind. es ist nicht erforderlich, mehr als ein [cfstr \_ File Contents](clipboard.md) -Format aufzuzählen. Wenn das Ziel wissen muss, wie viele dieser Formate das Datenobjekt enthält, kann das Ziel diese Informationen aus dem zugehörigen cfstr \_ File Descriptor-Format abrufen. Weitere Informationen zur Implementierung von **IDataObject:: enumformatusw**. finden Sie in der Referenz Dokumentation der-Methode.

### <a name="getdata-method"></a>GetData-Methode

Das Ziel ruft [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) auf, um ein bestimmtes Datenformat zu extrahieren. Das Ziel gibt das Format an, indem es die entsprechende [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur übergibt. **IDataObject:: GetData** gibt die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur des Formats zurück.

Das Ziel kann den **TYMED** -Member der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur auf einen bestimmten TYMED \_ *xxx* -Wert festlegen, um anzugeben, welcher Datenübertragungsmechanismus zum Extrahieren der Daten verwendet werden soll. Das Ziel kann jedoch auch eine allgemeinere Anforderung erstellen und das Datenobjekt entscheiden lassen. Um das Datenobjekt zum Auswählen des Datenübertragungsmechanismus aufzufordern, legt das Ziel alle von \_ ihm unterstützten TYMED *xxx* -Werte fest. [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) wählt einen dieser Datenübertragungs Mechanismen aus und gibt die entsprechende [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zurück. Beispielsweise ist **TYMED** häufig auf TYMED \_ HGLOBAL \| TYMED \_ IStream \| TYMED IStorage festgelegt, \_ um einen der drei Shell-Datenübertragungs Mechanismen anzufordern.

> [!Note]  
> Da es mehrere [cfstr \_ File Content](clipboard.md) -Formate geben kann, reichen die Member " **cfFormat** " und " **TYMED** " der [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur nicht aus, um anzugeben, welche [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur " [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) " zurückgeben soll. Für das Format cfstr \_ File Contents muss **IDataObject:: GetData** auch den **Lindex** -Member der **FORMATETC** -Struktur untersuchen, um die korrekte **STGMEDIUM** -Struktur zurückzugeben.

 

Das [cfstr \_ indragloop](clipboard.md) -Format wird in Datenobjekten eingefügt, sodass Ziele den Status der Drag & Drop-Schleife überprüfen und gleichzeitig das speicherintensive Rendering der Objektdaten vermeiden können. Die Daten des Formats sind ein **DWORD** -Wert, der auf einen Wert ungleich 0 (null) festgelegt wird, wenn sich das Datenobjekt innerhalb einer Drag-Schleife befindet. Der Datenwert des Formats wird auf 0 (null) festgelegt, wenn die Daten gelöscht wurden. Wenn ein Ziel dieses Format anfordert und es nicht von der Quelle geladen wurde, sollte [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) so reagieren, als ob die Quelle das Format mit dem Wert 0 (null) geladen hätte.

Während sich der Cursor über dem Zielfenster befindet, kann das Ziel das Drag & amp; [Drop-Hilfsobjekt](#using-the-drag-and-drop-helper-object) verwenden, um das Zieh Bild anzugeben. Das Drag & amp; Drop Helper-Objekt ruft [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) auf, um private Formate in das Datenobjekt zu laden, das für prozessübergreifende Unterstützung verwendet wird. Später wird [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) aufgerufen, um Sie abzurufen. Zur Unterstützung des Drag & Drop-Hilfsobjekts muss Ihre shelldatenobjektimplementierung in der Lage sein, beliebige private Formate zurückzugeben, wenn Sie angefordert werden.

### <a name="implementing-idropsource"></a>Implementieren von IDropSource

Die Quelle muss ein Objekt erstellen, das eine [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht. Diese Schnittstelle ermöglicht es der Quelle, das Zieh *Bild* zu aktualisieren, das die aktuelle Position des Cursors angibt, und dem System Feedback zu geben, wie ein Drag & Drop-Vorgang beendet wird. **IDropSource** verfügt über zwei Methoden: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) und [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback-Methode

In der Drag-Schleife ist eine Ablage Quelle dafür zuständig, die Cursorposition zu verfolgen und ein entsprechendes Zieh Bild anzuzeigen. In einigen Fällen möchten Sie jedoch möglicherweise die Darstellung des Zieh Bilds ändern, wenn es sich über dem Ablage Zielfenster befindet.

Wenn der Cursor das Zielfenster eingibt oder verlässt und während er sich über das Zielfenster bewegt, ruft das System regelmäßig die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Ziels auf. Das Ziel antwortet mit einem [**dropffect**](../com/dropeffect-constants.md) -Wert, der über die [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) -Methode an die Quelle weitergeleitet wird. Wenn dies der Grund ist, kann die Quelle die Darstellung des Cursors basierend auf dem **dropffect** -Wert ändern. Weitere Informationen finden Sie in den Referenzen zu **GiveFeedback** und [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

### <a name="querycontinuedrag-method"></a>QueryContinueDrag-Methode

Diese Methode wird aufgerufen, wenn sich der Mauszeiger-oder Tastatur Zustand ändert, während sich das Datenobjekt in der Drag-Schleife befindet. Es benachrichtigt die Quelle, ob die ESC-Taste gedrückt wurde, und gibt den aktuellen Zustand der Tastatur-Modifizierertasten an, z. b. STRG oder UMSCHALT. Der Rückgabewert der [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) -Methode gibt eine von drei Aktionen an:

-   S \_ OK. Fortsetzen des Zieh Vorgangs
-   DragDrop \_ S \_ Drop. Löschen Sie die Daten. Das System ruft dann die [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode des Ziels auf.
-   DragDrop \_ S \_ Abbrechen. Beenden Sie die Drag-Schleife, ohne die Daten zu löschen. Dieser Wert wird normalerweise zurückgegeben, wenn die Escape-Taste gedrückt wurde.

Weitere Informationen finden Sie in den Referenzen [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) und [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

## <a name="how-a-target-handles-a-data-object"></a>Verarbeiten eines Datenobjekts durch ein Ziel

Das Ziel empfängt ein Datenobjekt, wenn das Datenobjekt entweder aus der Zwischenablage abgerufen wird oder es vom Benutzer im Zielfenster abgelegt wurde. Das Ziel kann dann Daten aus dem Datenobjekt extrahieren. Bei Bedarf kann das Ziel das Datenobjekt auch über das Ergebnis des Vorgangs benachrichtigen. Vor einer shelldatenübertragung muss sich ein Ablage Ziel für den Vorgang vorbereiten:

1.  Das Ziel muss [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) aufrufen, um einen gültigen Zwischenablage-Format Wert für alle shellformate (außer [CF \_ HDROP](clipboard.md)) zu erhalten, die möglicherweise im Datenobjekt enthalten sind. CF \_ HDROP ist bereits ein gültiges Zwischenablage Format und muss nicht registriert werden.
2.  Um einen Drag & Drop-Vorgang zu unterstützen, muss das Ziel eine [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle implementieren und ein Zielfenster registrieren. Zum Registrieren eines Zielfensters Ruft das Ziel [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) auf und übergibt das Fenster Handle und den **IDropTarget** -Schnittstellen Zeiger.

Bei Übertragungen von Zwischenablage empfängt das Ziel keine Benachrichtigung, dass ein Datenobjekt in der Zwischenablage abgelegt wurde. In der Regel wird eine Anwendung benachrichtigt, dass ein Objekt von einer Benutzeraktion in der Zwischenablage gespeichert wird, z. b. durch Klicken auf die Schaltfläche Einfügen auf der Symbolleiste der Anwendung. Das Ziel ruft dann den [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Zeiger des Datenobjekts aus der Zwischenablage ab, indem [**olegetclipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard)aufgerufen wird. Bei Drag & Drop-Datenübertragungen verwendet das System die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Ziels, um dem Ziel Informationen zum Fortschritt der Datenübertragung bereitzustellen:

-   Das System ruft [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) auf, wenn der Cursor in das Zielfenster eintritt.
-   Das System ruft in regelmäßigen Abständen [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) auf, wenn der Cursor über das Zielfenster verläuft, um dem Ziel die aktuelle Cursorposition zu übergeben.
-   Das System ruft [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) auf, wenn der Cursor das Zielfenster verlässt.
-   Das System ruft [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) auf, wenn der Benutzer das Datenobjekt im Zielfenster löscht.

Eine Erläuterung der Implementierung dieser Methoden finden Sie unter [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Wenn die Daten gelöscht werden, stellt [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) dem Ziel einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts bereit. Das Ziel verwendet dann diese Schnittstelle, um Daten aus dem Datenobjekt zu extrahieren.

### <a name="extracting-shell-data-from-a-data-object"></a>Extrahieren von shelldaten aus einem Datenobjekt

Nachdem ein Datenobjekt gelöscht oder aus der Zwischenablage abgerufen wurde, kann das Ziel die benötigten Daten extrahieren. Der erste Schritt im Extraktionsprozess besteht in der Regel darin, die im Datenobjekt enthaltenen Formate aufzulisten:

-   Rufen Sie [**IDataObject:: enumformatusw**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). auf. Das Datenobjekt erstellt ein Standardmäßiges OLE-Enumerationsobjekt und gibt einen Zeiger auf seine [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) -Schnittstelle zurück.
-   Verwenden Sie die [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) -Methoden, um die Formate aufzulisten, die im Datenobjekt enthalten sind. Dieser Vorgang ruft in der Regel eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur für jedes Format ab, das das Objekt enthält. Das Enumerationsobjekt gibt jedoch normalerweise nur eine einzelne **FORMATETC** -Struktur für das [cfstr \_ File Contents](clipboard.md) -Format zurück, unabhängig davon, wie viele dieser Formate im Datenobjekt enthalten sind.
-   Wählen Sie ein oder mehrere Formate aus, die extrahiert werden sollen, und speichern Sie Ihre [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Strukturen.

Wenn Sie ein bestimmtes Format abrufen möchten, übergeben Sie die zugeordnete [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur an [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Diese Methode gibt eine [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur zurück, die Zugriff auf die Daten bereitstellt. Wenn Sie einen bestimmten Datenübertragungsmechanismus angeben möchten, legen Sie den Wert " **TYMED** " der **FORMATETC** -Struktur auf den entsprechenden Wert von "TYMED \_ *xxx* " fest. Um das Datenobjekt zum Auswählen eines Datenübertragungsmechanismus aufzufordern, legt das Ziel die TYMED \_ *xxx* -Werte für jeden Datenübertragungsmechanismus fest, der vom Ziel verarbeitet werden kann. Das Datenobjekt wählt einen dieser Datenübertragungs Mechanismen aus und gibt die entsprechende **STGMEDIUM** -Struktur zurück.

Bei den meisten Formaten kann das Ziel die Daten abrufen, indem es die [**formatierte**](/windows/win32/api/objidl/ns-objidl-formatetc) Struktur übergibt, die beim Auflisten der verfügbaren Formate empfangen wurde. Eine Ausnahme von dieser Regel ist " [cfstr \_ File Content](clipboard.md)". Da ein Datenobjekt mehrere Instanzen dieses Formats enthalten kann, entspricht die vom Enumerator zurückgegebene **FORMATETC** -Struktur möglicherweise nicht dem speziellen Format, das Sie extrahieren möchten. Zusätzlich zur Angabe der Member " **cfFormat** " und " **TYMED** " müssen Sie auch das **Lindex** -Element auf den Indexwert der Datei festlegen. Weitere Informationen finden Sie im Abschnitt *Verwenden des cfstr \_ File Contents-Formats zum Extrahieren von Daten aus einer Datei* im Abschnitt [Handling Shell Datenübertragung Szenarios](datascenarios.md)

Der Daten Extraktionsprozess hängt vom Typ des Zeigers ab, der in der zurückgegebenen [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur enthalten ist. Wenn die Struktur einen Zeiger auf eine [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) -oder [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) -Schnittstelle enthält, verwenden Sie die Schnittstellen Methoden, um die Daten zu extrahieren. Der Prozess des Extrahierens von Daten aus einem globalen Speicher Objekt wird im nächsten Abschnitt erläutert.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Extrahieren eines globalen Speicher Objekts aus einem Datenobjekt

Viele der shelldatenformate sind in Form eines globalen Speicher Objekts. Verwenden Sie das folgende Verfahren, um ein Format zu extrahieren, das ein globales Speicher Objekt aus einem Datenobjekt enthält, und weisen Sie die zugehörigen Daten einer lokalen Variablen zu:

1.  Erstellen Sie eine [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -Struktur. Legen Sie den **cfFormat** -Member auf den entsprechenden Zwischenablage Formatwert und den **TYMED** -Member auf TYMED \_ HGLOBAL fest.
2.  Erstellen Sie eine leere [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur.
3.  Rufen Sie [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)auf, und übergeben Sie Zeiger auf die [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) -und [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Strukturen.

    Wenn [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) zurückgegeben wird, enthält die [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur einen Zeiger auf das globale Speicher Objekt, das die Daten enthält.

4.  Weisen Sie die Daten einer lokalen Variablen zu, indem Sie [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) aufrufen und den **HGLOBAL** -Member der [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) -Struktur übergeben.
5.  Nennen Sie [**globalunlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) , um die Sperre für das globale Speicher Objekt freizugeben.
6.  Aufrufen von [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) , um das globale Speicher Objekt freizugeben.

> [!Note]  
> Sie müssen [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) verwenden, um das globale Speicher Objekt freizugeben, nicht [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree).

 

Im folgenden Beispiel wird gezeigt, wie ein **DWORD** -Wert extrahiert wird, der als globales Speicher Objekt aus einem Datenobjekt gespeichert wird. Der Parameter " **pdtobj** " ist ein Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts, " **CF** " ist das Zwischenablage Format, das die gewünschten Daten identifiziert, und " **pdwout** " wird verwendet, um den Datenwert zurückzugeben.


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

Das System verwendet die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle für die Kommunikation mit dem Ziel, während sich der Cursor über dem Zielfenster befindet. Die Ziel Antworten werden über die [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle an die Quelle weitergeleitet. Abhängig von der Antwort kann die Quelle das Symbol ändern, das die Daten darstellt. Wenn das Ablage Ziel das Daten Symbol angeben muss, können Sie hierfür ein [Drag & Drop-Hilfsobjekt](#using-the-drag-and-drop-helper-object)erstellen.

Bei herkömmlichen Drag & Drop-Vorgängen informiert das Ziel das Datenobjekt über das Ergebnis des Vorgangs, indem der *pdweffect* -Parameter von [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) auf den entsprechenden [**droetffect**](../com/dropeffect-constants.md) -Wert festgelegt wird. Bei shelldatenobjekten muss das Ziel möglicherweise auch [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata)aufrufen. Eine Erläuterung dazu, wie Ziele auf verschiedene Datenübertragungs Szenarien reagieren sollten, finden Sie unter [Handling Shell Datenübertragung Szenarios](datascenarios.md).

In den folgenden Abschnitten wird kurz erläutert, wie die Methoden [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)und [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) implementiert werden. Weitere Informationen finden Sie in der Referenz Dokumentation.

### <a name="dragenter-method"></a>DragEnter-Methode

Das System ruft die [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) -Methode auf, wenn der Cursor in das Zielfenster eintritt. Die zugehörigen Parameter stellen dem Ziel den Speicherort des Cursors, den Zustand der Tastatur-Modifizierertasten, z. b. die STRG-Taste, und einen Zeiger auf die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts bereit. Das Ziel ist dafür verantwortlich, dass diese Schnittstelle verwendet wird, um zu bestimmen, ob Sie keines der im Datenobjekt enthaltenen Formate annehmen kann. Wenn dies möglich ist, bleibt der Wert von *pdweffect* normalerweise unverändert. Wenn keine Daten aus dem Datenobjekt akzeptiert werden können, wird der Parameter *pdweffect* auf dropffect None festgelegt \_ . Das System übergibt den Wert dieses Parameters an die [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) -Schnittstelle des Datenobjekts, damit das entsprechende Zieh Bild angezeigt werden kann.

Ziele sollten die [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) -Methode nicht verwenden, um shelldaten vor dem Löschen zu Rendering. Das vollständige Rendering der Daten des Objekts für jedes derartige vorkommen kann dazu führen, dass der Zieh Cursor nicht mehr angezeigt wird. Um dieses Problem zu vermeiden, enthalten einige Shellobjekte ein [cfstr \_ indragloop](clipboard.md) -Format. Durch das Extrahieren dieses Formats können Ziele den Status der Drag-Schleife überprüfen und gleichzeitig das speicherintensive Rendering der Objektdaten vermeiden. Der Datenwert des Formats ist ein **DWORD** , das auf einen Wert ungleich 0 (null) festgelegt wird, wenn sich das Datenobjekt innerhalb einer Drag-Schleife befindet. Der Datenwert des Formats wird auf 0 (null) festgelegt, wenn die Daten gelöscht wurden.

Wenn das Ziel Daten aus dem Datenobjekt akzeptieren kann, sollte es **grfkeystate** überprüfen, um zu bestimmen, ob Modifizierertasten gedrückt wurden, um das normale Ablage Verhalten zu ändern. Der Standard Vorgang ist z. b. in der Regel eine Verschiebung, aber das Drücken der STRG-Taste weist normalerweise auf einen Kopiervorgang hin.

Während sich der Cursor über dem Zielfenster befindet, kann das Ziel das Drag & amp; [Drop-Hilfsobjekt](#using-the-drag-and-drop-helper-object) verwenden, um das Zieh Bild des Datenobjekts durch ein eigenes zu ersetzen. Wenn dies der Fall ist, sollte [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) [**idroptargethelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) aufgerufen werden, um die in den *DragEnter* -Parametern enthaltenen Informationen an das Drag & amp; Drop-Hilfsobjekt zu übergeben.

### <a name="dragover-method"></a>DragOver-Methode

Wenn der Cursor innerhalb des Zielfensters bewegt wird, ruft das System regelmäßig die [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) -Methode auf. Mit den zugehörigen Parametern wird das Ziel mit der Position des Cursors und dem Zustand der Tastatur Modifizierertasten, z. b. STRG-Taste, bereitgestellt. **IDropTarget::D ragover** hat weitgehend dieselben Zuständigkeiten wie [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), und die Implementierungen sind normalerweise sehr ähnlich.

Wenn das Ziel das Drag & amp; Drop-Hilfsobjekt verwendet, muss [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) [**idroptargethelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) anrufen, um die in den *DragOver* -Parametern enthaltenen Informationen an das Drag & amp; Drop-Hilfsobjekt weiterzuleiten.

### <a name="drop-method"></a>Drop-Methode

Das System ruft die [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) -Methode auf, um das Ziel zu benachrichtigen, dass der Benutzer die Daten gelöscht hat. Dies geschieht in der Regel durch Freigeben der Maustaste. **IDropTarget::D ROP** hat dieselben Parameter wie [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). Das Ziel antwortet normalerweise durch Extrahieren eines oder mehrerer Formate aus dem Datenobjekt. Wenn der Vorgang abgeschlossen ist, sollte das Ziel den Parameter " *pdweffect* " auf einen [**dropffect**](../com/dropeffect-constants.md) -Wert festlegen, der das Ergebnis des Vorgangs angibt. Für einige Arten von shelldatenübertragungen muss das Ziel auch [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) aufrufen, um ein Format mit zusätzlichen Informationen zum Ergebnis des Vorgangs an das Datenobjekt zu übergeben. Eine ausführliche Erläuterung finden Sie unter [Handling Shell Datenübertragung Szenarios](datascenarios.md).

Wenn das Ziel das Drag & amp; Drop-Hilfsobjekt verwendet, sollte [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) [**idroptargethelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) aufgerufen werden, um die in den [**idroptargethelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) -Parametern enthaltenen Informationen an das Drag & amp; Drop Helper-Objekt weiterzuleiten.

## <a name="using-the-drag-and-drop-helper-object"></a>Verwenden des Drag & amp; Drop-Hilfsobjekts

Das Drag & amp; Drop-Hilfsobjekt (CLSID \_ DragDropHelper) wird von der Shell exportiert, damit Ziele das Zieh Bild angeben können, während es sich über dem Zielfenster befindet. Wenn Sie das Drag & amp; Drop-Hilfsobjekt verwenden möchten, erstellen Sie ein in-Process-Server Objekt, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit einem Klassen Bezeichner (CLSID) von CLSID \_ DragDropHelper aufrufen. Das Drag & amp; Drop-Hilfsobjekt macht zwei Schnittstellen verfügbar, die wie folgt verwendet werden:

-   Die [**idragsourcehelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) -Schnittstelle ermöglicht dem Ablage Ziel, ein Symbol anzugeben, das das Datenobjekt darstellt.
-   Die [**idroptargethelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) -Schnittstelle ermöglicht dem Ablage Ziel, das Drag & Drop-Hilfsobjekt der Cursorposition zu informieren und das Daten Symbol anzuzeigen oder auszublenden.

### <a name="using-the-idragsourcehelper-interface"></a>Verwenden der idragsourcehelper-Schnittstelle

Die [**idragsourcehelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) -Schnittstelle wird vom Drag & amp; Drop-Hilfsobjekt verfügbar gemacht, damit ein Ablage Ziel das Bild bereitstellen kann, das angezeigt wird, während sich der Cursor über dem Zielfenster befindet. **Idragsourcehelper** bietet zwei alternative Möglichkeiten, um die Bitmap anzugeben, die als Drag-Bild verwendet werden soll:

-   Ablage Ziele, die über ein Fenster verfügen, können eine di \_ GetDragImage-Fenster Meldung für diese registrieren, indem Sie das Drag & amp; Drop-Hilfsobjekt mit [**idragsourcehelper:: initializefromwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow)initialisieren. Wenn das Ziel eine di \_ GetDragImage-Nachricht empfängt, fügt der Handler die Bitmapinformationen des Zieh Bilds in die [**shdragimage**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) -Struktur ein, die als *LPARAM* -Wert der Nachricht übergeben wird.
-   Fensterlose Ablage Ziele geben eine Bitmap an, wenn Sie das Drag & amp; Drop-Hilfsobjekt mit [**idragsourcehelper:: initializefrombitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap)initialisieren.

### <a name="using-the-idroptargethelper-interface"></a>Verwenden der idroptargethelper-Schnittstelle

Diese Schnittstelle ermöglicht dem Ablage Ziel, das Drag & amp; Drop-Hilfsobjekt zu benachrichtigen, wenn der Cursor in das Ziel wechselt oder das Ziel verlässt. Während sich der Cursor über dem Zielfenster befindet, ermöglicht [**idroptargethelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) das Ziel dem Ziel, dem Drag & Drop-Hilfsobjekt die Informationen zu übergeben, die das Ziel über seine [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle empfängt.

Vier der [**idroptargethelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) -Methoden –[**idroptargethelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**idroptargethelper::D ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**idroptargethelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)und [**idroptargethelper::D ROP**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)– sind der [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Methode mit demselben Namen zugeordnet. Um das Drag & amp; Drop-Hilfsobjekt zu verwenden, sollte jede der **IDropTarget** -Methoden die entsprechende **idroptargethelper** -Methode zum Weiterleiten der Informationen an das Drag & amp; Drop-Hilfsobjekt abrufen. Die fünfte **idroptargethelper** -Methode, [**idroptargethelper:: Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), benachrichtigt das Drag & amp; Drop-Hilfsobjekt, das Zieh Bild anzuzeigen oder auszublenden. Diese Methode wird verwendet, wenn ein Zielfenster in einem Videomodus mit niedriger Farbtiefe gezogen wird. Dies ermöglicht es dem Ziel, das Zieh Bild beim Zeichnen des Fensters auszublenden.

 

 
