---
description: Programmieren von DirectX mit com.
title: Programmieren von DirectX mit com
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: f712e5fed19d6afe2762a77ffcdf8b5977f85901
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "103961037"
---
# <a name="programming-directx-with-com"></a>Programmieren von DirectX mit com

Beim Microsoft-Component Object Model (com) handelt es sich um ein objektorientiertes Programmiermodell, das von verschiedenen Technologien verwendet wird, einschließlich des Massen Vorgangs der DirectX-API-Oberfläche. Aus diesem Grund verwenden Sie (als DirectX-Entwickler) beim Programmieren von DirectX unweigerlich com.

> [!NOTE]
> Das Thema Verwenden von [com-Komponenten mit C++/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) zeigt, wie Sie mit [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/)DirectX-APIs (und eine beliebige com-API) verwenden. Das ist die einfachste und empfohlene Technologie, die Sie verwenden können.

Alternativ dazu können Sie auch unformatierte com verwenden, und das ist das, was in diesem Thema erläutert wird. Sie benötigen grundlegende Kenntnisse über die Prinzipien und Programmiertechniken, die bei der Nutzung von COM-APIs beteiligt sind. Obwohl com den Ruf hat, schwierig und komplex zu sein, ist die für die meisten DirectX-Anwendungen erforderliche com-Programmierung unkompliziert. Dies liegt teilweise daran, dass Sie die von DirectX bereitgestellten com-Objekte verbrauchen. Es ist nicht erforderlich, eigene COM-Objekte zu erstellen, was in der Regel die Komplexität ergibt.

## <a name="com-component-overview"></a>Übersicht über COM-Komponenten

Ein COM-Objekt ist im Wesentlichen eine gekapselte Komponente von Funktionen, die von Anwendungen verwendet werden kann, um eine oder mehrere Tasks auszuführen. Für die Bereitstellung werden mindestens eine COM-Komponente in eine Binärdatei mit dem Namen com-Server gepackt. häufiger als eine DLL.

Eine herkömmliche dll exportiert kostenlose Funktionen. Ein com-Server kann dasselbe tun. Die COM-Komponenten innerhalb des COM-Servers machen jedoch COM-Schnittstellen und Mitglieds Methoden verfügbar, die zu diesen Schnittstellen gehören. Die Anwendung erstellt Instanzen von COM-Komponenten, ruft Schnittstellen von Ihnen ab und ruft Methoden für diese Schnittstellen auf, um von den in den COM-Komponenten implementierten Funktionen zu profitieren.

In der Praxis ist dies vergleichbar mit dem Aufrufen von Methoden für ein reguläres C++-Objekt. Es gibt jedoch einige Unterschiede.

- Ein COM-Objekt erzwingt eine strengere Kapselung als ein C++-Objekt. Sie können das Objekt nicht einfach erstellen und dann eine beliebige öffentliche Methode abrufen. Stattdessen werden die öffentlichen Methoden einer COM-Komponente in eine oder mehrere COM-Schnittstellen gruppiert. Zum Aufrufen einer Methode erstellen Sie das-Objekt und rufen aus dem-Objekt die-Schnittstelle ab, die die-Methode implementiert. Eine Schnittstelle implementiert in der Regel einen zugehörigen Satz von Methoden, die Zugriff auf eine bestimmte Funktion des Objekts ermöglichen. Die [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) -Schnittstelle stellt z. b. einen virtuellen Grafikadapter dar und enthält Methoden, die Ihnen das Erstellen von Ressourcen ermöglichen, z. b. und viele andere Adapter bezogene Aufgaben.
- Ein COM-Objekt wird nicht auf die gleiche Weise wie ein C++-Objekt erstellt. Es gibt mehrere Möglichkeiten, ein COM-Objekt zu erstellen, aber alle umfassen com-spezifische Techniken. Die DirectX-API umfasst eine Vielzahl von Hilfsfunktionen und-Methoden, die das Erstellen der meisten DirectX-com-Objekte vereinfachen.
- Sie müssen com-spezifische Techniken verwenden, um die Lebensdauer eines COM-Objekts zu steuern.
- Der com-Server (in der Regel eine DLL) muss nicht explizit geladen werden. Sie können auch nicht mit einer statischen Bibliothek verknüpfen, um eine COM-Komponente zu verwenden. Jede COM-Komponente verfügt über einen eindeutigen registrierten Bezeichner (einen global eindeutigen Bezeichner oder eine GUID), der von Ihrer Anwendung verwendet wird, um das COM-Objekt zu identifizieren. Die-Komponente wird von der Anwendung identifiziert, und die com-Laufzeit lädt automatisch die korrekte com-Server-DLL.
- COM ist eine binäre Spezifikation. COM-Objekte können in einer Vielzahl von Sprachen geschrieben und darauf zugegriffen werden. Sie müssen nichts über den Quellcode des Objekts wissen. Beispielsweise verwenden Visual Basic Anwendungen regelmäßig com-Objekte, die in C++ geschrieben wurden.

## <a name="component-object-and-interface"></a>Komponente, Objekt und Schnittstelle

Es ist wichtig, den Unterschied zwischen Komponenten, Objekten und Schnittstellen zu verstehen. Bei der zufälligen Verwendung werden Sie möglicherweise eine Komponente oder ein Objekt mit dem Namen der Prinzipal Schnittstelle, auf die verwiesen wird, hören. Die Begriffe sind jedoch nicht austauschbar. Eine Komponente kann eine beliebige Anzahl von Schnittstellen implementieren. und ein Objekt ist eine Instanz einer Komponente. Wenn z. b. alle Komponenten die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)implementieren müssen, implementieren Sie normalerweise mindestens eine zusätzliche Schnittstelle, und Sie können viele implementieren.

Wenn Sie eine bestimmte Schnittstellen Methode verwenden möchten, dürfen Sie nicht nur ein Objekt instanziieren, sondern auch die richtige Schnittstelle daraus abrufen.

Darüber hinaus können mehr als eine Komponente dieselbe Schnittstelle implementieren. Eine Schnittstelle ist eine Gruppe von Methoden, die einen logisch zusammen gehörigen Satz von Vorgängen ausführen. Die Schnittstellen Definition gibt nur die Syntax der Methoden und ihrer allgemeinen Funktionalität an. Jede COM-Komponente, die einen bestimmten Satz von Vorgängen unterstützen muss, kann dies durch Implementieren einer geeigneten Schnittstelle erreichen. Einige Schnittstellen sind hochgradig spezialisiert und werden nur von einer einzelnen Komponente implementiert. andere sind in einer Vielzahl von Situationen nützlich und werden von vielen Komponenten implementiert.

Wenn eine Komponente eine Schnittstelle implementiert, muss Sie jede Methode in der Schnittstellen Definition unterstützen. Anders ausgedrückt: Sie müssen in der Lage sein, jede beliebige Methode aufzurufen und sicher zu sein, dass Sie vorhanden ist. Die Details der Implementierung einer bestimmten Methode können sich jedoch von einer Komponente zu einer anderen unterscheiden. Beispielsweise können unterschiedliche-Komponenten andere Algorithmen verwenden, um am Endergebnis zu gelangen. Es gibt auch keine Garantie dafür, dass eine Methode auf nicht triviale Weise unterstützt wird. Manchmal implementiert eine Komponente eine häufig verwendete Schnittstelle, aber Sie muss nur eine Teilmenge der Methoden unterstützen. Sie können die restlichen Methoden weiterhin erfolgreich aufzurufen, aber Sie geben ein [**HRESULT**](#hresult-values) (einen com-Standard Typ, der einen Ergebniscode darstellt) zurück, der den Wert **E_NOTIMPL** enthält. In der Dokumentation finden Sie Informationen dazu, wie eine Schnittstelle von einer bestimmten Komponente implementiert wird.

Der com-Standard erfordert, dass eine Schnittstellen Definition nicht geändert werden darf, sobald Sie veröffentlicht wurde. Der Autor kann z. b. eine neue Methode nicht zu einer vorhandenen Schnittstelle hinzufügen. Der Autor muss stattdessen eine neue Schnittstelle erstellen. Es gibt zwar keine Einschränkungen bezüglich der Methoden, die sich in dieser Schnittstelle befinden müssen, eine gängige Vorgehensweise besteht jedoch darin, dass die Schnittstelle der nächsten Generation alle Methoden der alten Schnittstelle sowie alle neuen Methoden enthält.

Es ist nicht ungewöhnlich, dass eine Schnittstelle mehrere Generationen hat. In der Regel führen alle Generationen im Wesentlichen die gleiche Gesamtaufgabe aus, aber Sie unterscheiden sich in den Besonderheiten. Häufig implementiert eine COM-Komponente jede aktuelle und vorherige Generierung der Herkunft einer bestimmten Schnittstelle. Auf diese Weise können ältere Anwendungen weiterhin die älteren Schnittstellen des Objekts verwenden, während neuere Anwendungen die Features der neueren Schnittstellen nutzen können. Normalerweise hat eine abstiegsgruppe von Schnittstellen denselben Namen und eine ganze Zahl, die die Generierung angibt. Wenn die ursprüngliche Schnittstelle z. b. den Namen **IMyInterface** hat (was Generation 1 impliziert), werden die nächsten zwei Generationen als " **IMyInterface2** " und " **IMyInterface3**" bezeichnet. Bei DirectX-Schnittstellen werden aufeinander folgende Generationen in der Regel für die Versionsnummer von DirectX benannt.

## <a name="guids"></a>GUIDs

GUIDs sind ein wichtiger Bestandteil des com-Programmiermodells. Bei der grundlegendsten ist eine GUID eine 128-Bit-Struktur. GUIDs werden jedoch auf eine Weise erstellt, um sicherzustellen, dass keine zwei GUIDs identisch sind. COM verwendet GUIDs für zwei primäre Zwecke ausgiebig.

- , Um eine bestimmte COM-Komponente eindeutig zu identifizieren. Eine GUID, die zum Identifizieren einer COM-Komponente zugewiesen wird, wird als Klassen Bezeichner (CLSID) bezeichnet, und Sie verwenden eine CLSID, wenn Sie eine Instanz der zugeordneten COM-Komponente erstellen möchten.
- , Um eine bestimmte COM-Schnittstelle eindeutig zu identifizieren. Eine GUID, die zum Identifizieren einer COM-Schnittstelle zugewiesen ist, wird als Schnittstellen Bezeichner (IID) bezeichnet, und Sie verwenden eine IID, wenn Sie eine bestimmte Schnittstelle von einer Instanz einer Komponente (ein Objekt) anfordern. Die IID einer Schnittstelle ist identisch, unabhängig davon, welche Komponente die Schnittstelle implementiert.

Die DirectX-Dokumentation bezieht sich in der Regel auf Komponenten und Schnittstellen anhand ihrer beschreibenden Namen (z. b. **ID3D12Device**) und nicht anhand ihrer GUIDs. Innerhalb des Kontexts der DirectX-Dokumentation gibt es keine Mehrdeutigkeit. Es ist technisch möglich, dass ein Drittanbieter eine Schnittstelle mit dem beschreibenden Namen " **ID3D12Device** " erstellt (er muss eine andere IID aufweisen, um gültig zu sein). Im Interesse der Übersichtlichkeit wird dies jedoch nicht empfohlen.

Der einzige eindeutige Weg, auf ein bestimmtes Objekt oder eine bestimmte Schnittstelle zu verweisen, ist die GUID.

Obwohl eine GUID eine Struktur ist, wird eine GUID häufig in einer äquivalenten Zeichen folgen Form ausgedrückt. Das allgemeine Format der Zeichen folgen Form einer GUID ist 32 hexadezimal Ziffern im Format 8-4-4-4-12. Das heißt, {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, wobei jedes x einer hexadezimal Ziffer entspricht. Die Zeichen folgen Form der IID für die **ID3D12Device** -Schnittstelle lautet z. b. {189819f 1-1db6-4b57-be54-1821339b85b85}.

Da die tatsächliche GUID etwas unscharf und leicht zu verwenden ist, wird normalerweise auch ein entsprechender Name bereitgestellt. In Ihrem Code können Sie diesen Namen anstelle der eigentlichen Struktur verwenden, wenn Sie Funktionen aufrufen, z. b. Wenn Sie ein Argument für den `riid` Parameter an [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)übergeben. Die übliche Benennungs Konvention besteht darin, entweder IID_ oder CLSID_ dem beschreibenden Namen der Schnittstelle bzw. des Objekts voranzustellen. Beispielsweise ist der Name der IID der **ID3D12Device** -Schnittstelle IID_ID3D12Device.

> [!NOTE]
> DirectX-Anwendungen sollten mit ``dxguid.lib`` und verknüpft werden ``uuid.lib`` , um Definitionen für die verschiedenen Schnittstellen-und Klassen-GUIDs bereitzustellen. Visual C++ und andere Compiler unterstützen die Spracherweiterung **__uuidof** Operators, aber eine explizite Verknüpfung im C-Stil mit diesen Linkbibliotheken wird ebenfalls unterstützt und ist vollständig portabel.

## <a name="hresult-values"></a>HRESULT-Werte

Die meisten com-Methoden geben eine 32-Bit-Ganzzahl mit dem Namen **HRESULT** zurück. Bei den meisten Methoden ist das HRESULT im Wesentlichen eine Struktur, die zwei primäre Informationsteile enthält.
- Gibt an, ob die Methode erfolgreich oder fehlerhaft war.
- Ausführlichere Informationen zum Ergebnis des Vorgangs, der von der-Methode ausgeführt wird.

Einige Methoden geben einen **HRESULT** -Wert aus dem Standardsatz zurück, der in definiert ist `Winerror.h` . Eine Methode kann jedoch einen benutzerdefinierten **HRESULT** -Wert mit spezielleren Informationen zurückgeben. Diese Werte sind in der Regel auf der Referenzseite der Methode dokumentiert.

Die Liste der **HRESULT** -Werte, die Sie auf der Referenzseite einer Methode finden, ist oft nur eine Teilmenge der möglichen Werte, die zurückgegeben werden können. Die Liste deckt in der Regel nur die Werte ab, die für die-Methode spezifisch sind, sowie die Standardwerte, die eine bestimmte Methoden spezifische Bedeutung haben. Sie sollten davon ausgehen, dass eine Methode möglicherweise eine Vielzahl von **HRESULT** -Standardwerten zurückgibt, auch wenn Sie nicht explizit dokumentiert werden.

Obwohl **HRESULT** -Werte häufig zum Zurückgeben von Fehlerinformationen verwendet werden, sollten Sie sich nicht als Fehlercodes vorstellen. Die Tatsache, dass das Bit, das den Erfolg oder Misserfolg angibt, getrennt von den Bits, die die detaillierten Informationen enthalten, gespeichert wird, ermöglicht **HRESULT** -Werten, eine beliebige Anzahl von Erfolgs-und Fehlercodes zu haben. Gemäß der Konvention werden den Namen von Erfolgs Codes s_ und Fehlercodes durch E_ vorangestellt. Die beiden am häufigsten verwendeten Codes sind z. b. S_OK und E_FAIL, die einen einfachen Erfolg bzw. Fehler angeben.

Die Tatsache, dass com-Methoden möglicherweise eine Vielzahl von Erfolgs-oder Fehlercodes zurückgeben, bedeutet, dass Sie sorgfältig darauf achten müssen, wie Sie den **HRESULT** -Wert testen. Stellen Sie sich z. b. eine hypothetische Methode mit dokumentierten Rückgabe Werten S_OK bei erfolgreicher Ausführung vor, und E_FAIL andernfalls. Beachten Sie jedoch, dass die Methode möglicherweise auch andere Fehler-oder Erfolgs Codes zurückgibt. Das folgende Code Fragment veranschaulicht die Gefahr der Verwendung eines einfachen Tests, wobei `hr` den **HRESULT** -Wert enthält, der von der-Methode zurückgegeben wird.

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Solange diese Methode im Falle eines Fehlers nur E_FAIL zurückgibt (und nicht in einem anderen Fehlercode), funktioniert dieser Test. Es ist jedoch realistischer, dass eine bestimmte Methode implementiert wird, um eine Reihe spezifischer Fehlercodes zurückzugeben, vielleicht E_NOTIMPL oder E_INVALIDARG. Mit dem obigen Code werden diese Werte fälschlicherweise als erfolgreich interpretiert.

Wenn Sie ausführliche Informationen zum Ergebnis des Methoden Aufrufes benötigen, müssen Sie jeden relevanten **HRESULT** -Wert testen. Sie sind jedoch möglicherweise nur daran interessiert, ob die Methode erfolgreich war oder fehlgeschlagen ist. Ein robuster Weg, um zu testen, ob ein **HRESULT** -Wert Erfolg oder Fehler angibt, besteht darin, den Wert an die folgenden Makros zu übergeben, die in WinError. h definiert sind.

- Das `SUCCEEDED` Makro gibt true für einen Erfolgs Code und false für einen Fehlercode zurück.
- Das `FAILED` -Makro gibt true für einen Fehlercode und false für einen Erfolgs Code zurück.

Daher können Sie das vorangehende Code Fragment mit dem- `FAILED` Makro beheben, wie im folgenden Code gezeigt.

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Dieses korrigierte Code Fragment behandelt E_NOTIMPL und E_INVALIDARG ordnungsgemäß als Fehler.

Obwohl die meisten com-Methoden strukturierte **HRESULT** -Werte zurückgeben, verwendet eine kleine Zahl das **HRESULT** , um eine einfache Ganzzahl zurückzugeben. Diese Methoden sind implizit immer erfolgreich. Wenn Sie ein **HRESULT** dieser Sortierung an das Makro "erfolgreich" übergeben, gibt das Makro immer "true" zurück. Ein Beispiel für eine häufig aufgerufene Methode, die kein **HRESULT** zurückgibt, ist die **IUnknown:: Release** -Methode, die einen Ulong-Wert zurückgibt. Diese Methode Dekremente den Verweis Zähler eines Objekts um 1 und gibt den aktuellen Verweis Zähler zurück. Eine Erörterung der Verweis Zählung finden Sie unter [Verwalten der Lebensdauer eines COM-Objekts](#managing-a-com-objects-lifetime) .

## <a name="the-address-of-a-pointer"></a>Die Adresse eines Zeigers.

Wenn Sie einige Referenzseiten der com-Methode anzeigen, werden Sie wahrscheinlich in etwa wie folgt ausgeführt.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Obwohl ein normaler Zeiger einem C/C++-Entwickler recht vertraut ist, verwendet com häufig eine zusätzliche Dereferenzierungsebene. Diese zweite Dereferenzierungsebene wird durch zwei Sternchen, `**` , nach der Typdeklaration und der Variablenname in der Regel über ein Präfix von angegeben `pp` . Bei der obigen Funktion wird der- `ppDevice` Parameter in der Regel als Adresse eines Zeigers auf eine void-Funktion bezeichnet. In der Praxis ist in diesem Beispiel `ppDevice` die Adresse eines Zeigers auf eine **ID3D12Device** -Schnittstelle.

Im Gegensatz zu einem C++-Objekt greifen Sie nicht direkt auf die Methoden eines COM-Objekts zu. Stattdessen müssen Sie einen Zeiger auf eine-Schnittstelle abrufen, die die-Methode verfügbar macht. Zum Aufrufen der-Methode verwenden Sie im Grunde die gleiche Syntax wie zum Aufrufen eines Zeigers auf eine C++-Methode. Wenn Sie z. b. die **IMyInterface::D osomething** -Methode aufrufen möchten, verwenden Sie die folgende Syntax.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

Die Notwendigkeit einer zweiten dereferenzierungsstufe ergibt sich aus der Tatsache, dass Sie keine Schnittstellen Zeiger direkt erstellen. Sie müssen eine der verschiedenen Methoden, wie z. b. die oben gezeigte **D3D12CreateDevice** -Methode, aufzurufen. Um eine solche Methode zum Abrufen eines Schnittstellen Zeigers zu verwenden, deklarieren Sie eine Variable als Zeiger auf die gewünschte Schnittstelle, und übergeben Sie dann die Adresse dieser Variablen an die-Methode. Das heißt, dass Sie die Adresse eines Zeigers an die-Methode übergeben. Wenn die-Methode zurückgibt, verweist die Variable auf die angeforderte Schnittstelle, und Sie können diesen Zeiger verwenden, um beliebige Methoden der Schnittstelle aufzurufen.

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>Erstellen eines COM-Objekts

Es gibt mehrere Möglichkeiten, ein COM-Objekt zu erstellen. Dies sind die beiden am häufigsten verwendeten in der DirectX-Programmierung.

- Indirekt durch Aufrufen einer DirectX-Methode oder Funktion, die das-Objekt für Sie erstellt. Die-Methode erstellt das-Objekt und gibt eine-Schnittstelle für das-Objekt zurück. Wenn Sie ein Objekt auf diese Weise erstellen, können Sie manchmal angeben, welche Schnittstelle zurückgegeben werden soll, und das andere Mal, wenn die Schnittstelle impliziert ist. Im obigen Codebeispiel wird gezeigt, wie ein COM-Objekt mit einem Direct3D 12-Gerät indirekt erstellt wird.
- Direkt, indem die CLSID des Objekts an die [**cokreateinstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben wird. Die-Funktion erstellt eine Instanz des-Objekts und gibt einen Zeiger auf eine-Schnittstelle zurück, die Sie angeben.

Wenn Sie ein COM-Objekt erstellen, müssen Sie ein com-initialisieren, indem Sie die [**CoInitializeEx-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufrufen. Wenn Sie Objekte indirekt erstellen, wird diese Aufgabe von der Objekt Erstellungs Methode verarbeitet. Wenn Sie jedoch ein Objekt mit **cokreateinstance** erstellen müssen, müssen Sie **CoInitializeEx** explizit aufrufen. Wenn Sie fertig sind, muss com durch Aufrufen von " [**aninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)" nicht initialisiert werden. Wenn Sie **CoInitializeEx** aufrufen, müssen Sie es mit einem **CallInitialize**-Befehl vergleichen. Anwendungen, die com explizit initialisieren müssen, führen dies in der Regel in der Start Routine aus, und die Initialisierung von com in der Bereinigungs Routine wird nicht durchzuführen.

Zum Erstellen einer neuen Instanz eines COM-Objekts mit **cokreateinstance** muss die CLSID des Objekts vorhanden sein. Wenn diese CLSID öffentlich verfügbar ist, finden Sie Sie in der Referenz Dokumentation oder in der entsprechenden Header Datei. Wenn die CLSID nicht öffentlich verfügbar ist, können Sie das Objekt nicht direkt erstellen.

Die **cokreateinzustance** -Funktion hat fünf Parameter. Für die COM-Objekte, die Sie mit DirectX verwenden, können Sie die Parameter normalerweise wie folgt festlegen.

*rclsid* Legen Sie diese Einstellung auf die CLSID des Objekts fest, das Sie erstellen möchten.

*pUnkOuter* Legen Sie auf fest `nullptr` . Dieser Parameter wird nur verwendet, wenn Sie-Objekte aggregierten. Eine Erörterung der com-Aggregation wird in diesem Thema nicht behandelt.

*dwClsContext* Legen Sie auf CLSCTX_INPROC_SERVER fest. Diese Einstellung gibt an, dass das Objekt als dll implementiert wird und im Rahmen des Anwendungsprozesses ausgeführt wird.

*riid* Legen Sie auf die IID der Schnittstelle fest, die zurückgegeben werden soll. Die Funktion erstellt das Objekt und gibt den angeforderten Schnittstellen Zeiger im PPV-Parameter zurück.

*PPV* Legen Sie diese Einstellung auf die Adresse eines Zeigers fest, der auf die durch angegebene Schnittstelle festgelegt wird, `riid` Wenn die Funktion zurückgibt. Diese Variable sollte als Zeiger auf die angeforderte Schnittstelle deklariert werden, und der Verweis auf den Zeiger in der Parameterliste sollte in (LPVOID *) umgewandelt werden.

Die indirekte Erstellung eines Objekts ist in der Regel viel einfacher, wie im obigen Codebeispiel gezeigt. Sie übergeben die Objekt Erstellungs Methode als Adresse eines Schnittstellen Zeigers, und die-Methode erstellt dann das-Objekt und gibt einen Schnittstellen Zeiger zurück. Wenn Sie ein Objekt indirekt erstellen, können Sie auch dann, wenn Sie nicht auswählen, welche Schnittstelle die Methode zurückgibt, häufig eine Vielzahl von Dingen angeben, wie das Objekt erstellt werden soll.

Beispielsweise können Sie an **D3D12CreateDevice** einen Wert übergeben, der die minimale D3D-Funktionsebene angibt, die vom zurückgegebenen Gerät unterstützt werden soll, wie im obigen Codebeispiel gezeigt.

## <a name="using-com-interfaces"></a>Mit COM-Schnittstellen

Wenn Sie ein COM-Objekt erstellen, gibt die Erstellungs Methode einen Schnittstellen Zeiger zurück. Sie können dann mit diesem Zeiger auf eine beliebige Methode der Schnittstelle zugreifen. Die Syntax ist identisch mit der, die mit einem Zeiger auf eine C++-Methode verwendet wird.

## <a name="requesting-additional-interfaces"></a>Anfordern zusätzlicher Schnittstellen

In vielen Fällen kann der Schnittstellen Zeiger, den Sie von der Erstellungs Methode erhalten, der einzige sein, den Sie benötigen. Tatsächlich ist es für ein Objekt relativ üblich, nur eine andere Schnittstelle als **IUnknown** zu exportieren. Viele-Objekte exportieren jedoch mehrere Schnittstellen, und Sie benötigen möglicherweise Zeiger auf einige von Ihnen. Wenn Sie mehr Schnittstellen benötigen, als von der Erstellungs Methode zurückgegeben werden, ist es nicht erforderlich, ein neues Objekt zu erstellen. Fordern Sie stattdessen einen weiteren Schnittstellen Zeiger mit der [**IUnknown:: QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))des Objekts an.

Wenn Sie Ihr Objekt mit **cokreateinstance** erstellen, können Sie einen **IUnknown** -Schnittstellen Zeiger anfordern und dann **IUnknown:: QueryInterface** aufrufen, um jede benötigte Schnittstelle anzufordern. Diese Vorgehensweise ist jedoch nicht geeignet, wenn Sie nur eine einzige Schnittstelle benötigen, und Sie funktioniert nicht, wenn Sie eine Objekt Erstellungs Methode verwenden, mit der Sie nicht angeben können, welcher Schnittstellen Zeiger zurückgegeben werden soll. In der Praxis müssen Sie in der Regel keinen expliziten **IUnknown** -Zeiger abrufen, da alle COM-Schnittstellen die **IUnknown** -Schnittstelle erweitern.

Das Erweitern einer Schnittstelle ähnelt konzeptionell der Vererbung von einer C++-Klasse. Die untergeordnete Schnittstelle macht alle Methoden der übergeordneten Schnittstelle sowie eine oder mehrere eigene verfügbar. Tatsächlich wird häufig "erbt von" anstelle von "Erweitert" angezeigt. Sie müssen daran denken, dass die Vererbung für das Objekt intern ist. Die Anwendung kann die Schnittstelle eines Objekts nicht erben oder erweitern. Allerdings können Sie die untergeordnete-Schnittstelle verwenden, um eine beliebige Methode des untergeordneten oder übergeordneten Elements aufzurufen.

Da alle Schnittstellen untergeordnete Elemente von **IUnknown** sind, können Sie **QueryInterface** für jeden der Schnittstellen Zeiger, den Sie bereits für das Objekt besitzen, aufgerufen werden. Wenn Sie dies tun, müssen Sie die IID der angeforderten Schnittstelle und die Adresse eines Zeigers angeben, der den Schnittstellen Zeiger enthält, wenn die Methode zurückgegeben wird.

Das folgende Code Fragment ruft z. b. **IDXGIFactory2:: kreateswapchainforhwnd** auf, um ein primäres Austausch Ketten Objekt zu erstellen. Dieses Objekt stellt mehrere Schnittstellen zur Verfügung. Die Methode " **kreateswapchainforhwnd** " gibt eine **IDXGISwapChain1** -Schnittstelle zurück. Der nachfolgende Code verwendet dann die **IDXGISwapChain1** -Schnittstelle, um **QueryInterface** aufzurufen, um eine **IDXGISwapChain3** -Schnittstelle anzufordern.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> In C++ können Sie das ``IID_PPV_ARGS`` -Makro anstelle des expliziten IID-und Cast-Zeigers verwenden: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Dies wird häufig für Erstellungs Methoden und **QueryInterface** verwendet. Weitere Informationen finden Sie unter " [combaseapi. h](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args) ".

## <a name="managing-a-com-objects-lifetime"></a>Verwalten der Lebensdauer eines COM-Objekts

Wenn ein Objekt erstellt wird, ordnet das System die erforderlichen Speicherressourcen zu. Wenn ein Objekt nicht mehr benötigt wird, sollte es zerstört werden. Das System kann diesen Arbeitsspeicher für andere Zwecke verwenden. Mit C++-Objekten können Sie die Lebensdauer des Objekts direkt mit den `new` `delete` Operatoren und Steuern, in Fällen, in denen Sie auf dieser Ebene arbeiten oder indem Sie die Stapel-und Bereichs Lebensdauer verwenden. COM ermöglicht keine direkte Erstellung oder Zerstörung von Objekten. Der Grund für diesen Entwurf ist, dass das gleiche Objekt von mehr als einem Teil der Anwendung oder in einigen Fällen durch mehr als eine Anwendung verwendet werden kann. Wenn einer dieser Verweise das Objekt zerstören würde, werden die anderen Verweise ungültig. Stattdessen verwendet com ein System der Verweis Zählung, um die Lebensdauer eines Objekts zu steuern.

Der Verweis Zähler eines Objekts gibt an, wie oft eine der Schnittstellen angefordert wurde. Jedes Mal, wenn eine Schnittstelle angefordert wird, wird der Verweis Zähler inkrementiert. Eine Anwendung gibt eine Schnittstelle frei, wenn diese Schnittstelle nicht mehr benötigt wird, und verringert den Verweis Zähler. Solange der Verweis Zähler größer als 0 (null) ist, verbleibt das Objekt im Arbeitsspeicher. Wenn der Verweis Zähler Null erreicht, zerstört sich das Objekt selbst. Sie müssen nichts über den Verweis Zähler eines Objekts wissen. Solange Sie die Schnittstellen eines Objekts ordnungsgemäß abrufen und freigeben, verfügt das Objekt über die entsprechende Lebensdauer.

Die ordnungsgemäße Handhabung der Verweis Zählung ist ein wesentlicher Bestandteil der com-Programmierung. Wenn dies nicht der Fall ist, können Sie problemlos einen Speicherfehler oder einen Absturz erzeugen. Einer der häufigsten Fehler, die com-Programmierer treffen, besteht darin, eine Schnittstelle nicht freizugeben. Wenn dies geschieht, erreicht der Verweis Zähler niemals NULL, und das Objekt bleibt unbegrenzt im Speicher.

> [!NOTE]
> Direct3D 10 oder höher hat leicht geänderte Lebensdauer Regeln für-Objekte. Insbesondere von Objekten, die von **ID3DxxDeviceChild** abgeleitet sind, wird Ihr übergeordnetes Gerät nicht mehr angezeigt (d. h., wenn die besitzende **ID3DxxDevice** auf den Wert 0 Ref count trifft, sind alle untergeordneten Objekte ebenfalls ebenfalls ungültig). Wenn Sie **Set** -Methoden verwenden, um Objekte an die renderpipeline zu binden, erhöhen diese Verweise den Verweis Zähler nicht (d. h., Sie sind schwache Verweise). In der Praxis ist dies am besten, indem Sie sicherstellen, dass alle untergeordneten Geräte Objekte vollständig freigegeben werden, bevor Sie das Gerät freigeben.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Inkrementieren und Dekrementieren des Verweis zähders

Wenn Sie einen neuen Schnittstellen Zeiger abrufen, muss der Verweis Zähler durch einen Aufruf von [**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)erhöht werden. Allerdings muss die Anwendung diese Methode in der Regel nicht aufzurufen. Wenn Sie einen Schnittstellen Zeiger abrufen, indem Sie eine Objekt Erstellungs Methode aufrufen, oder indem Sie **IUnknown:: QueryInterface** aufrufen, erhöht das Objekt automatisch den Verweis Zähler. Wenn Sie jedoch einen Schnittstellen Zeiger auf andere Weise erstellen, z. b. Kopieren eines vorhandenen Zeigers, müssen Sie **IUnknown:: adressf** explizit aufruft. Wenn Sie andernfalls den ursprünglichen Schnittstellen Zeiger freigeben, wird das Objekt möglicherweise zerstört, auch wenn Sie möglicherweise noch die Kopie des Zeigers verwenden müssen.

Sie müssen alle Schnittstellen Zeiger freigeben, unabhängig davon, ob Sie oder das Objekt den Verweis Zähler inkrementiert haben. Wenn Sie keinen Schnittstellen Zeiger mehr benötigen, wenden Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) an, um den Verweis Zähler zu verringern. Eine gängige Vorgehensweise besteht darin, alle Schnittstellen Zeiger auf zu initialisieren `nullptr` und Sie dann wieder auf festzulegen, `nullptr` Wenn Sie freigegeben werden. Mit dieser Konvention können Sie alle Schnittstellen Zeiger im Bereinigungs Code testen. Diese sind noch nicht `nullptr` aktiv, und Sie müssen Sie freigeben, bevor Sie die Anwendung beenden.

Das folgende Code Fragment erweitert das oben gezeigte Beispiel, um zu veranschaulichen, wie die Verweis Zählung behandelt werden soll.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>Intelligente com-Zeiger

Der bisherige Code hat explizit ``Release`` und zum Verwalten ``AddRef`` der Verweis Zähler mithilfe von **IUnknown** -Methoden aufgerufen. Dieses Muster erfordert, dass der Programmierer sorgfältig daran interessiert ist, die Anzahl in allen möglichen Codepath beizubehalten. Dies kann zu einer komplizierten Fehlerbehandlung führen, und mit aktivierter C++-Ausnahmebehandlung kann es besonders schwierig sein, diese zu implementieren. Eine bessere Lösung mit C++ ist die Verwendung eines [intelligenten Zeigers](/cpp/cpp/smart-pointers-modern-cpp).

* **WinRT:: com_ptr** ist ein intelligenter Zeiger, der durch die [C++/WinRT-sprach Projektionen](/uwp/cpp-ref-for-winrt/com-ptr)bereitgestellt wird. Dies ist der empfohlene com-Zeiger, der für UWP-Apps verwendet werden soll. Beachten Sie, dass für C++/WinRT C++ 17 erforderlich ist.

* **Microsoft:: WRL:: comptr** ist ein intelligenter Zeiger, der von der [Windows-Runtime C++ Template Library (WRL)](/cpp/cppcx/wrl/comptr-class)bereitgestellt wird. Diese Bibliothek ist "Pure" C++ und kann daher für Windows-Runtime Anwendungen (über C++/CX oder C++/WinRT) sowie für klassische Win32-Desktop Anwendungen verwendet werden. Dieser intelligente Zeiger funktioniert auch für ältere Versionen von Windows, die die Windows-Runtime-APIs nicht unterstützen. Für Win32-Desktop Anwendungen können Sie verwenden, ``#include <wrl/client.h>`` um nur diese Klasse einzuschließen und optional auch das Präprozessorsymbol zu definieren ``__WRL_CLASSIC_COM_STRICT__`` . Weitere Informationen finden Sie unter Überprüfen von [intelligenten com-Zeigern](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited).

* **CComPtr** ist ein intelligenter Zeiger, der vom [Active Template Library (ATL)](/cpp/atl/reference/ccomptr-class)bereitgestellt wird. **Microsoft:: WRL:: comptr** ist eine neuere Version dieser Implementierung, die eine Reihe von Problemen mit der geringfügigen Verwendung behandelt. Daher wird die Verwendung dieses intelligenten Zeigers nicht für neue Projekte empfohlen. Weitere Informationen finden Sie unter [Erstellen und Verwenden von CComPtr und CComQIPtr](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances).


## <a name="using-atl-with-directx-9"></a>Verwenden von ATL mit DirectX 9

Wenn Sie die Active Template Library (ATL) mit DirectX 9 verwenden möchten, müssen Sie die Schnittstellen für die ATL-Kompatibilität neu definieren. Dies ermöglicht es Ihnen, die **CComQIPtr** -Klasse ordnungsgemäß zu verwenden, um einen Zeiger auf eine Schnittstelle zu erhalten.

Sie wissen, ob Sie die Schnittstellen für ATL nicht neu definieren, da die folgende Fehlermeldung angezeigt wird.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

Im folgenden Codebeispiel wird gezeigt, wie die idirectxfiledata-Schnittstelle definiert wird.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Nachdem Sie die Schnittstelle neu definiert haben, müssen Sie die **Attach** -Methode verwenden, um die Schnittstelle an den von zurückgegebenen Schnittstellen Zeiger anzufügen **::D irect3dcreate9**. Wenn Sie dies nicht tun, wird die **IDirect3D9** -Schnittstelle von der intelligenten Zeiger Klasse nicht ordnungsgemäß freigegeben.

Die **CComPtr** -Klasse ruft intern **IUnknown:: adressf** für den Schnittstellen Zeiger auf, wenn das Objekt erstellt wird und eine Schnittstelle der **CComPtr** -Klasse zugewiesen wird. Um das Verlust des Schnittstellen Zeigers zu vermeiden, dürfen Sie nicht * * IUnknown:: adressf für die von zurückgegebene Schnittstelle aufzurufen **::D irect3dcreate9**.

Der folgende Code gibt die-Schnittstelle ordnungsgemäß frei, ohne **IUnknown:: adressf** zu aufrufen.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Verwenden Sie den vorherigen Code. Verwenden Sie den folgenden Code nicht, der " **IUnknown:: adressf** " gefolgt von " **IUnknown:: Release**" aufruft und den von hinzugefügten Verweis nicht freigibt **::D irect3dcreate9**.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Beachten Sie, dass dies die einzige Stelle in Direct3D 9 ist, an der Sie die **Attach** -Methode auf diese Weise verwenden müssen.

Weitere Informationen zu den **CComPtr** -und **CComQIPtr** -Klassen finden Sie in ihren Definitionen in der `Atlbase.h` Header Datei.
