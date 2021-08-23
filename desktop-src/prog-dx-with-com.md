---
description: Programmieren von DirectX mit COM.
title: Programmieren von DirectX mit COM
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 660f030e56d0b84325f7b90a9e2cc8e3864587660dd452611f41c78241220f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600200"
---
# <a name="programming-directx-with-com"></a>Programmieren von DirectX mit COM

Microsoft Component Object Model (COM) ist ein objektorientiertes Programmiermodell, das von mehreren Technologien verwendet wird, einschließlich des Großteils der DirectX-API-Oberfläche. Aus diesem Grund verwenden Sie (als DirectX-Entwickler) zwangsläufig COM, wenn Sie DirectX programmieren.

> [!NOTE]
> Im Thema Consume COM components with C++/WinRT (Nutzen von COM-Komponenten mit [C++/WinRT)](/windows/uwp/cpp-and-winrt-apis/consume-com) wird gezeigt, wie DirectX-APIs (und alle COM-APIs) mithilfe von [C++/WinRT verwendet werden.](/windows/uwp/cpp-and-winrt-apis/) Dies ist die mit Abstand bequemste und empfohlene Technologie.

Alternativ können Sie UN-COM verwenden, und darum geht es in diesem Thema. Sie benötigen ein grundlegendes Verständnis der Prinzipien und Programmiertechniken für die Nutzung von COM-APIs. Obwohl COM den Ruf hat, schwierig und komplex zu sein, ist die com-Programmierung, die für die meisten DirectX-Anwendungen erforderlich ist, unkompliziert. Dies liegt zum Teil daran, dass Sie die von DirectX bereitgestellten COM-Objekte nutzen. Sie müssen keine eigenen COM-Objekte erstellen. In der Regel entsteht die Komplexität.

## <a name="com-component-overview"></a>Übersicht über COM-Komponenten

Ein COM-Objekt ist im Wesentlichen eine gekapselte Komponente der Funktionalität, die von Anwendungen verwendet werden kann, um eine oder mehrere Aufgaben auszuführen. Für die Bereitstellung werden eine oder mehrere COM-Komponenten in eine Binärdatei gepackt, die als COM-Server bezeichnet wird. häufiger als keine DLL.

Eine herkömmliche DLL exportiert kostenlose Funktionen. Ein COM-Server kann dies auch tun. Die COM-Komponenten auf dem COM-Server machen jedoch COM-Schnittstellen und Membermethoden verfügbar, die zu diesen Schnittstellen gehören. Ihre Anwendung erstellt Instanzen von COM-Komponenten, ruft Schnittstellen von ihnen ab und ruft Methoden für diese Schnittstellen auf, um von den in den COM-Komponenten implementierten Funktionen zu profitieren.

In der Praxis ähnelt dies dem Aufrufen von Methoden für ein reguläres C++-Objekt. Es gibt jedoch einige Unterschiede.

- Ein COM-Objekt erzwingt eine strengere Kapselung als ein C++-Objekt. Sie können nicht einfach das -Objekt erstellen und dann eine beliebige öffentliche Methode aufrufen. Stattdessen werden die öffentlichen Methoden einer COM-Komponente in eine oder mehrere COM-Schnittstellen eingeteilt. Zum Aufrufen einer Methode erstellen Sie das -Objekt und rufen aus dem -Objekt die Schnittstelle ab, die die -Methode implementiert. Eine Schnittstelle implementiert in der Regel einen verwandten Satz von Methoden, die Zugriff auf ein bestimmtes Feature des Objekts bereitstellen. Beispielsweise stellt die [**ID3D12Device-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) einen virtuellen Grafikadapter dar und enthält Methoden, mit denen Sie Ressourcen erstellen können, z. B. und viele andere adapterbezogene Aufgaben.
- Ein COM-Objekt wird nicht auf die gleiche Weise wie ein C++-Objekt erstellt. Es gibt mehrere Möglichkeiten, ein COM-Objekt zu erstellen, aber alle umfassen COM-spezifische Techniken. Die DirectX-API enthält eine Vielzahl von Hilfsfunktionen und -methoden, die die Erstellung der meisten DirectX-COM-Objekte vereinfachen.
- Sie müssen COM-spezifische Techniken verwenden, um die Lebensdauer eines COM-Objekts zu steuern.
- Der COM-Server (in der Regel eine DLL) muss nicht explizit geladen werden. Sie können auch keine Verknüpfung mit einer statischen Bibliothek erstellen, um eine COM-Komponente zu verwenden. Jede COM-Komponente verfügt über einen eindeutigen registrierten Bezeichner (einen global eindeutigen Bezeichner oder eine GUID), den Ihre Anwendung zum Identifizieren des COM-Objekts verwendet. Ihre Anwendung identifiziert die Komponente, und die COM-Runtime lädt automatisch die richtige COM-Server-DLL.
- COM ist eine binäre Spezifikation. COM-Objekte können in einer Vielzahl von Sprachen geschrieben und aufgerufen werden. Sie müssen nichts über den Quellcode des Objekts wissen. Beispielsweise verwenden Visual Basic-Anwendungen routinemäßig COM-Objekte, die in C++ geschrieben wurden.

## <a name="component-object-and-interface"></a>Komponente, Objekt und Schnittstelle

Es ist wichtig, den Unterschied zwischen Komponenten, Objekten und Schnittstellen zu verstehen. Bei der gelegentlichen Verwendung hören Sie möglicherweise eine Komponente oder ein Objekt, auf die bzw. das durch den Namen der Prinzipalschnittstelle verwiesen wird. Die Begriffe sind jedoch nicht austauschbar. Eine Komponente kann eine beliebige Anzahl von Schnittstellen implementieren. und ein -Objekt ist eine Instanz einer Komponente. Während beispielsweise alle Komponenten die [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)implementieren müssen, implementieren sie normalerweise mindestens eine zusätzliche Schnittstelle und können viele implementieren.

Um eine bestimmte Schnittstellenmethode zu verwenden, müssen Sie nicht nur ein Objekt instanziieren, sondern auch die richtige Schnittstelle daraus abrufen.

Darüber hinaus können mehrere Komponenten die gleiche Schnittstelle implementieren. Eine Schnittstelle ist eine Gruppe von Methoden, die einen logisch verwandten Satz von Vorgängen ausführen. Die Schnittstellendefinition gibt nur die Syntax der Methoden und ihre allgemeine Funktionalität an. Jede COM-Komponente, die einen bestimmten Satz von Vorgängen unterstützen muss, kann dazu eine geeignete Schnittstelle implementieren. Einige Schnittstellen sind hochgradig spezialisiert und werden nur von einer einzelnen Komponente implementiert. andere sind in einer Vielzahl von Situationen nützlich und werden von vielen Komponenten implementiert.

Wenn eine Komponente eine Schnittstelle implementiert, muss sie jede Methode in der Schnittstellendefinition unterstützen. Anders ausgedrückt: Sie müssen eine beliebige Methode aufrufen können und sicher sein, dass sie vorhanden ist. Die Details der Art und Weise, wie eine bestimmte Methode implementiert wird, können jedoch von Komponente zu Komponente variieren. Beispielsweise können verschiedene Komponenten unterschiedliche Algorithmen verwenden, um zum Endergebnis zu gelangen. Es gibt auch keine Garantie, dass eine Methode auf nichttriviale Weise unterstützt wird. Manchmal implementiert eine Komponente eine häufig verwendete Schnittstelle, muss aber nur eine Teilmenge der Methoden unterstützen. Sie können die verbleibenden Methoden weiterhin erfolgreich aufrufen, aber sie geben ein [**HRESULT**](#hresult-values) (ein COM-Standardtyp, der einen Ergebniscode darstellt) zurück, das den Wert **E_NOTIMPL.** Informationen dazu, wie eine Schnittstelle von einer bestimmten Komponente implementiert wird, finden Sie in der Dokumentation.

Der COM-Standard erfordert, dass sich eine Schnittstellendefinition nicht ändern darf, nachdem sie veröffentlicht wurde. Der Autor kann beispielsweise einer vorhandenen Schnittstelle keine neue Methode hinzufügen. Der Autor muss stattdessen eine neue Schnittstelle erstellen. Obwohl es keine Einschränkungen hinsichtlich der Methoden gibt, die sich in dieser Schnittstelle befinden müssen, ist es üblich, dass die Schnittstelle der nächsten Generation alle Methoden der alten Schnittstelle sowie alle neuen Methoden enthält.

Es ist nicht ungewöhnlich, dass eine Schnittstelle mehrere Generationen hat. In der Regel führen alle Generationen im Wesentlichen die gleiche Allgemeine Aufgabe aus, aber sie unterscheiden sich in bestimmten Bereichen. Häufig implementiert eine COM-Komponente jede aktuelle und vorherige Generierung der Überführung einer bestimmten Schnittstelle. Dadurch können ältere Anwendungen weiterhin die älteren Schnittstellen des Objekts verwenden, während neuere Anwendungen die Features der neueren Schnittstellen nutzen können. In der Regel hat eine Abstiegsgruppe von Schnittstellen den gleichen Namen sowie eine ganze Zahl, die die Generierung angibt. Wenn die ursprüngliche Schnittstelle z. B. **IMyInterface** genannt wird (was Generation 1 impliziert), würden die nächsten beiden Generationen **IMyInterface2** und **IMyInterface3 heißen.** Bei DirectX-Schnittstellen werden nachfolgende Generationen in der Regel nach der Versionsnummer von DirectX benannt.

## <a name="guids"></a>GUIDs

GUIDs sind ein wichtiger Bestandteil des COM-Programmiermodells. Im Grundlegendsten ist eine GUID eine 128-Bit-Struktur. GUIDs werden jedoch so erstellt, dass sichergestellt ist, dass keine zwei GUIDs identisch sind. COM verwendet GUIDs häufig für zwei primäre Zwecke.

- Um eine bestimmte COM-Komponente eindeutig zu identifizieren. Eine GUID, die zugewiesen wird, um eine COM-Komponente zu identifizieren, wird als Klassenbezeichner (CLSID) bezeichnet, und Sie verwenden eine CLSID, wenn Sie eine Instanz der zugeordneten COM-Komponente erstellen möchten.
- Um eine bestimmte COM-Schnittstelle eindeutig zu identifizieren. Eine GUID, die zum Identifizieren einer COM-Schnittstelle zugewiesen wird, wird als Schnittstellenbezeichner (Interface Identifier, IID) bezeichnet, und Sie verwenden eine IID, wenn Sie eine bestimmte Schnittstelle von einer Instanz einer Komponente (einem -Objekt) anfordern. Die IID einer Schnittstelle ist identisch, unabhängig davon, welche Komponente die Schnittstelle implementiert.

Der Einfachheit halber bezieht sich die DirectX-Dokumentation normalerweise auf Komponenten und Schnittstellen mit ihren beschreibenden Namen (z. B. **ID3D12Device)** und nicht mit ihren GUIDs. Im Kontext der DirectX-Dokumentation gibt es keine Mehrdeutigkeit. Es ist technisch möglich, dass ein Drittanbieter eine Schnittstelle mit dem beschreibenden Namen **ID3D12Device** erstellen kann (es müsste eine andere IID sein, um gültig zu sein). Aus Gründen der Übersichtlichkeit wird dies jedoch nicht empfohlen.

Die einzige eindeutige Möglichkeit, auf ein bestimmtes Objekt oder eine bestimmte Schnittstelle zu verweisen, ist also die GUID.

Obwohl eine GUID eine -Struktur ist, wird eine GUID häufig in äquivalenter Zeichenfolgenform ausgedrückt. Das allgemeine Format der Zeichenfolgenform einer GUID ist 32 Hexadezimalziffern im Format 8-4-4-4-12. Das heißt{ xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, wobei jedes x einer Hexadezimalziffer entspricht. Die Zeichenfolgenform der IID für die **ID3D12Device-Schnittstelle** ist beispielsweise {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Da die tatsächliche GUID etwas unlässig zu verwenden und leicht zu falsch eingeben ist, wird in der Regel auch ein entsprechender Name bereitgestellt. In Ihrem Code können Sie diesen Namen anstelle der tatsächlichen Struktur verwenden, wenn Sie Funktionen aufrufen, z. B. wenn Sie ein Argument für den -Parameter `riid` [**an D3D12CreateDevice übergeben.**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) Die benutzerdefinierte Benennungskonvention besteht im Vor- IID_ oder CLSID_ beschreibenden Namen der Schnittstelle bzw. des Objekts. Beispielsweise ist der Name der IID der **ID3D12Device-Schnittstelle** IID_ID3D12Device.

> [!NOTE]
> DirectX-Anwendungen sollten mit ``dxguid.lib`` und ``uuid.lib`` verknüpfen, um Definitionen für die verschiedenen Schnittstellen- und Klassen-GUIDs zur Verfügung zu stellen. Visual C++ und andere Compiler unterstützen  die __uuidof-Operatorspracherweiterung, aber die explizite Verknüpfung im C-Stil mit diesen Linkbibliotheken wird ebenfalls unterstützt und vollständig portabel.

## <a name="hresult-values"></a>HRESULT-Werte

Die meisten COM-Methoden geben eine 32-Bit-Ganzzahl namens **HRESULT zurück.** Bei den meisten Methoden ist HRESULT im Wesentlichen eine Struktur, die zwei primäre Informationen enthält.
- Gibt an, ob die Methode erfolgreich war oder fehlgeschlagen ist.
- Ausführlichere Informationen zum Ergebnis des von der -Methode ausgeführten Vorgangs.

Einige Methoden geben einen **HRESULT-Wert** aus dem in definierten Standardsatz `Winerror.h` zurück. Eine Methode kann jedoch einen benutzerdefinierten **HRESULT-Wert** mit spezielleren Informationen zurückgeben. Diese Werte werden normalerweise auf der Referenzseite der Methode dokumentiert.

Die Liste der **HRESULT-Werte,** die Sie auf der Referenzseite einer Methode finden, ist häufig nur eine Teilmenge der möglichen Werte, die zurückgegeben werden können. Die Liste deckt in der Regel nur die Werte ab, die spezifisch für die Methode sind, sowie die Standardwerte, die eine methodenspezifische Bedeutung haben. Sie sollten davon ausgehen, dass eine Methode eine Vielzahl von **HRESULT-Standardwerten** zurückgeben kann, auch wenn sie nicht explizit dokumentiert sind.

**Obwohl HRESULT-Werte** häufig verwendet werden, um Fehlerinformationen zurückzugeben, sollten Sie sich diese nicht als Fehlercodes vorstellen. Die Tatsache, dass das Bit, das auf Erfolg oder Fehler hinweist, getrennt von den Bits gespeichert wird, die die ausführlichen Informationen enthalten, ermöglicht **HRESULT-Werten** eine beliebige Anzahl von Erfolgs- und Fehlercodes. Der Konvention nach werden den Namen von Erfolgscodes S_ und Fehlercodes durch E_ vorangestellt. Die beiden am häufigsten verwendeten Codes sind beispielsweise S_OK und E_FAIL, die auf einen einfachen Erfolg bzw. Fehler hinweisen.

Die Tatsache, dass COM-Methoden eine Vielzahl von Erfolgs- oder Fehlercodes zurückgeben können, bedeutet, dass Sie darauf achten müssen, wie Sie den **HRESULT-Wert** testen. Betrachten Sie beispielsweise eine hypothetische Methode mit dokumentierten Rückgabewerten von S_OK , falls erfolgreich, und E_FAIL andernfalls . Denken Sie jedoch daran, dass die Methode möglicherweise auch andere Fehler- oder Erfolgscodes zurückgibt. Das folgende Codefragment veranschaulicht die Gefahr der Verwendung eines einfachen Tests, bei dem `hr` den von der -Methode zurückgegebenen **HRESULT-Wert** enthält.

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

Solange diese Methode im Fehlerfall immer nur E_FAIL (und keinen anderen Fehlercode) zurückgibt, funktioniert dieser Test. Es ist jedoch realistischer, dass eine bestimmte Methode implementiert wird, um bestimmte Fehlercodes zurückzugeben, z. B. E_NOTIMPL oder E_INVALIDARG. Mit dem obigen Code werden diese Werte fälschlicherweise als Erfolg interpretiert.

Wenn Sie ausführliche Informationen zum Ergebnis des Methodenaufrufs benötigen, müssen Sie jeden relevanten **HRESULT-Wert** testen. Möglicherweise interessieren Sie sich jedoch nur dafür, ob die Methode erfolgreich war oder fehlgeschlagen ist. Eine robuste Möglichkeit, zu testen, ob ein **HRESULT-Wert** auf Erfolg oder Fehler hinweist, besteht darin, den Wert an eines der folgenden Makros zu übergeben, die in Winerror.h definiert sind.

- Das `SUCCEEDED` Makro gibt TRUE für einen Erfolgscode und FALSE für einen Fehlercode zurück.
- Das `FAILED` Makro gibt TRUE für einen Fehlercode und FALSE für einen Erfolgscode zurück.

Daher können Sie das vorangehende Codefragment mithilfe des `FAILED` Makros korrigieren, wie im folgenden Code gezeigt.

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

Dieses korrigierte Codefragment behandelt E_NOTIMPL und E_INVALIDARG ordnungsgemäß als Fehler.

Obwohl die meisten COM-Methoden strukturierte **HRESULT-Werte** zurückgeben, verwendet eine kleine Zahl **HRESULT,** um eine einfache ganze Zahl zurückzugeben. Implizit sind diese Methoden immer erfolgreich. Wenn Sie ein **HRESULT** dieser Art an das SUCCEEDED-Makro übergeben, gibt das Makro immer TRUE zurück. Ein Beispiel für eine häufig aufgerufene Methode, die kein **HRESULT** zurückgibt, ist die **IUnknown::Release-Methode,** die eine ULONG zurückgibt. Diese Methode dekrementiert den Verweiszähler eines Objekts um eins und gibt den aktuellen Verweiszähler zurück. Eine Erläuterung der Verweiszählung finden Sie unter Verwalten der [Lebensdauer eines COM-Objekts.](#managing-a-com-objects-lifetime)

## <a name="the-address-of-a-pointer"></a>Die Adresse eines Zeigers

Wenn Sie einige COM-Methodenverweisseiten anzeigen, werden Sie wahrscheinlich in etwa wie folgt ausführen.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Während ein normaler Zeiger jedem C/C++-Entwickler recht vertraut ist, verwendet COM häufig eine zusätzliche Dekonstruktionsebene. Diese zweite Dekonstruktionsebene wird durch zwei Sternchen ( `**` ) nach der Typdeklaration angegeben, und der Variablenname hat in der Regel das Präfix `pp` . Für die obige Funktion wird der `ppDevice` Parameter in der Regel als Adresse eines Zeigers auf ein void bezeichnet. In der Praxis ist in diesem Beispiel `ppDevice` die Adresse eines Zeigers auf eine **ID3D12Device-Schnittstelle.**

Im Gegensatz zu einem C++-Objekt greifen Sie nicht direkt auf die Methoden eines COM-Objekts zu. Stattdessen müssen Sie einen Zeiger auf eine Schnittstelle abrufen, die die -Methode verfügbar macht. Um die -Methode aufzurufen, verwenden Sie im Wesentlichen die gleiche Syntax wie beim Aufrufen eines Zeigers auf eine C++-Methode. Um beispielsweise die **IMyInterface::D oSomething-Methode** aufzurufen, verwenden Sie die folgende Syntax.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

Die Notwendigkeit einer zweiten Dekonstruktionsebene ergibt sich aus der Tatsache, dass Sie schnittstellenzeiger nicht direkt erstellen. Sie müssen eine der verschiedenen Methoden aufrufen, z. B. die oben **gezeigte D3D12CreateDevice-Methode.** Um eine solche Methode zum Abrufen eines Schnittstellenzeigers zu verwenden, deklarieren Sie eine Variable als Zeiger auf die gewünschte Schnittstelle und übergeben dann die Adresse dieser Variablen an die -Methode. Anders ausgedrückt: Sie übergeben die Adresse eines Zeigers an die -Methode. Wenn die Methode zurückgegeben wird, zeigt die Variable auf die angeforderte Schnittstelle, und Sie können diesen Zeiger verwenden, um eine der Methoden der Schnittstelle aufzurufen.

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

Es gibt mehrere Möglichkeiten, ein COM-Objekt zu erstellen. Dies sind die beiden am häufigsten bei der DirectX-Programmierung verwendeten.

- Indirekt durch Aufrufen einer DirectX-Methode oder -Funktion, die das -Objekt für Sie erstellt. Die -Methode erstellt das -Objekt und gibt eine Schnittstelle für das -Objekt zurück. Wenn Sie ein Objekt auf diese Weise erstellen, können Sie manchmal angeben, welche Schnittstelle zurückgegeben werden soll, andernfalls wird die Schnittstelle impliziert. Im obigen Codebeispiel wird veranschaulicht, wie indirekt ein DIRECT3D 12-Geräte-COM-Objekt erstellt wird.
- Direkt, indem die CLSID des Objekts an die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)übergeben wird. Die Funktion erstellt eine Instanz des -Objekts und gibt einen Zeiger auf eine schnittstelle zurück, die Sie angeben.

Einmal müssen Sie COM initialisieren, bevor Sie COM-Objekte erstellen, indem Sie die [**CoInitializeEx-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)aufrufen. Wenn Sie Objekte indirekt erstellen, übernimmt die Objekterstellungsmethode diese Aufgabe. Wenn Sie jedoch ein Objekt mit **CoCreateInstance** erstellen müssen, müssen Sie **CoInitializeEx** explizit aufrufen. Wenn Sie fertig sind, muss COM durch Aufrufen von [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)nicht initialisiert werden. Wenn Sie **CoInitializeEx** aufrufen, müssen Sie ihn mit einem Aufruf von **CoUninitialize abgleichen.** Anwendungen, die COM explizit initialisieren müssen, tun dies in der Regel in ihrer Startroutine, und sie aufheben die Initialisierung von COM in ihrer Bereinigungsroutine.

Um eine neue Instanz eines COM-Objekts mit **CoCreateInstance** zu erstellen, benötigen Sie die CLSID des Objekts. Wenn diese CLSID öffentlich verfügbar ist, finden Sie sie in der Referenzdokumentation oder in der entsprechenden Headerdatei. Wenn die CLSID nicht öffentlich verfügbar ist, können Sie das Objekt nicht direkt erstellen.

Die **CoCreateInstance-Funktion** verfügt über fünf Parameter. Für die COM-Objekte, die Sie mit DirectX verwenden, können Sie die Parameter normalerweise wie folgt festlegen.

*rclsid* Legen Sie diese auf die CLSID des Objekts fest, das Sie erstellen möchten.

*pUnkOuter* Legen Sie auf `nullptr` fest. Dieser Parameter wird nur verwendet, wenn Sie Objekte aggregieren. Eine Erläuterung der COM-Aggregation liegt außerhalb des Rahmens dieses Themas.

*dwClsContext* Legen Sie auf CLSCTX_INPROC_SERVER fest. Diese Einstellung gibt an, dass das Objekt als DLL implementiert und als Teil des Anwendungsprozesses ausgeführt wird.

*riid* Legen Sie auf die IID der Schnittstelle fest, die Zurückgegeben werden soll. Die Funktion erstellt das -Objekt und gibt den angeforderten Schnittstellenzeiger im ppv-Parameter zurück.

*ppv* Legen Sie dies auf die Adresse eines Zeigers fest, der auf die Schnittstelle festgelegt wird, die von angegeben `riid` wird, wenn die Funktion zurückgegeben wird. Diese Variable sollte als Zeiger auf die angeforderte Schnittstelle deklariert werden, und der Verweis auf den Zeiger in der Parameterliste sollte in (LPVOID *) geändert werden.

Das indirekte Erstellen eines Objekts ist in der Regel viel einfacher, wie im obigen Codebeispiel zu sehen. Sie übergeben die Objekterstellungsmethode an die Adresse eines Schnittstellenzeigers, und die Methode erstellt dann das Objekt und gibt einen Schnittstellenzeiger zurück. Wenn Sie indirekt ein Objekt erstellen, auch wenn Sie nicht auswählen können, welche Schnittstelle von der Methode zurückgegeben wird, können Sie häufig trotzdem eine Vielzahl von Dingen darüber angeben, wie das Objekt erstellt werden soll.

Beispielsweise können Sie an **D3D12CreateDevice** einen Wert übergeben, der die minimale D3D-Featureebene angibt, die das zurückgegebene Gerät unterstützen soll, wie im obigen Codebeispiel gezeigt.

## <a name="using-com-interfaces"></a>Verwenden von COM-Schnittstellen

Wenn Sie ein COM-Objekt erstellen, gibt die Erstellungsmethode einen Schnittstellenzeiger zurück. Sie können diesen Zeiger dann verwenden, um auf die Methoden der Schnittstelle zuzugreifen. Die Syntax ist identisch mit der Syntax, die mit einem Zeiger auf eine C++-Methode verwendet wird.

## <a name="requesting-additional-interfaces"></a>Anfordern zusätzlicher Schnittstellen

In vielen Fällen ist der Schnittstellenzeiger, den Sie von der Erstellungsmethode erhalten, möglicherweise der einzige, den Sie benötigen. Tatsächlich ist es relativ üblich, dass ein Objekt nur eine andere Schnittstelle als **IUnknown** exportiert. Viele Objekte exportieren jedoch mehrere Schnittstellen, und Sie benötigen möglicherweise Zeiger auf mehrere von ihnen. Wenn Sie mehr Schnittstellen als die von der Erstellungsmethode zurückgegebene benötigen, ist es nicht erforderlich, ein neues -Objekt zu erstellen. Fordern Sie stattdessen einen anderen Schnittstellenzeiger an, indem Sie die [**IUnknown::QueryInterface-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))des Objekts verwenden.

Wenn Sie Ihr Objekt mit **CoCreateInstance** erstellen, können Sie einen **IUnknown-Schnittstellenzeiger** anfordern und dann **IUnknown::QueryInterface** aufrufen, um jede benötigte Schnittstelle anzufordern. Dieser Ansatz ist jedoch unpraktisch, wenn Sie nur eine einzige Schnittstelle benötigen, und er funktioniert überhaupt nicht, wenn Sie eine Objekterstellungsmethode verwenden, mit der Sie nicht angeben können, welcher Schnittstellenzeiger zurückgegeben werden soll. In der Praxis müssen Sie in der Regel keinen expliziten **IUnknown-Zeiger** abrufen, da alle COM-Schnittstellen die **IUnknown-Schnittstelle** erweitern.

Das Erweitern einer Schnittstelle ähnelt konzeptionell dem Erben von einer C++-Klasse. Die untergeordnete Schnittstelle macht alle Methoden der übergeordneten Schnittstelle sowie mindestens eine eigene verfügbar. Tatsächlich wird häufig "erbt von" anstelle von "erweitert" verwendet. Beachten Sie, dass die Vererbung für das Objekt intern ist. Ihre Anwendung kann nicht von der Schnittstelle eines Objekts erben oder diese erweitern. Sie können jedoch die untergeordnete Schnittstelle verwenden, um eine der Methoden des untergeordneten oder übergeordneten Elements aufzurufen.

Da alle Schnittstellen untergeordnete Elemente von **IUnknown** sind, können Sie **QueryInterface** für jeden schnittstellenzeiger aufrufen, den Sie bereits für das Objekt haben. Wenn Sie dies tun, müssen Sie die IID der angeforderten Schnittstelle und die Adresse eines Zeigers angeben, der den Schnittstellenzeiger enthält, wenn die Methode zurückgegeben wird.

Das folgende Codefragment ruft beispielsweise **IDXGIFactory2::CreateSwapChainForHwnd** auf, um ein primäres Swap chain-Objekt zu erstellen. Dieses Objekt macht mehrere Schnittstellen verfügbar. Die **CreateSwapChainForHwnd-Methode** gibt eine **IDXGISwapChain1-Schnittstelle** zurück. Der nachfolgende Code verwendet dann die **IDXGISwapChain1-Schnittstelle** zum Aufrufen **von QueryInterface** zum Anfordern einer **IDXGISwapChain3-Schnittstelle.**

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
> In C++ können Sie das Makro anstelle der expliziten IID und des ``IID_PPV_ARGS`` Cast-Zeigers verwenden: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Dies wird häufig für Erstellungsmethoden sowie für **QueryInterface verwendet.** Weitere Informationen finden Sie unter [combaseapi.h.](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)

## <a name="managing-a-com-objects-lifetime"></a>Verwalten der Lebensdauer eines COM-Objekts

Wenn ein Objekt erstellt wird, ordnet das System die erforderlichen Arbeitsspeicherressourcen zu. Wenn ein Objekt nicht mehr benötigt wird, sollte es zerstört werden. Das System kann diesen Arbeitsspeicher für andere Zwecke verwenden. Mit C++-Objekten können Sie die Lebensdauer des Objekts direkt mit den Operatoren und steuern, wenn Sie auf dieser Ebene oder einfach die Stapel- und Bereichslebensdauer `new` `delete` verwenden. COM ermöglicht es Ihnen nicht, Objekte direkt zu erstellen oder zu zerstören. Der Grund für diesen Entwurf ist, dass dasselbe Objekt von mehr als einem Teil der Anwendung oder in einigen Fällen von mehr als einer Anwendung verwendet werden kann. Wenn einer dieser Verweise das Objekt zerstören würde, wären die anderen Verweise ungültig. Stattdessen verwendet COM ein System der Verweiszählung, um die Lebensdauer eines Objekts zu steuern.

Die Verweisanzahl eines Objekts gibt an, wie oft eine seiner Schnittstellen angefordert wurde. Jedes Mal, wenn eine Schnittstelle angefordert wird, wird die Verweisanzahl erhöht. Eine Anwendung gibt eine Schnittstelle frei, wenn diese Schnittstelle nicht mehr benötigt wird, und dekrementieren die Verweisanzahl. Solange die Verweisanzahl größer als 0 (null) ist, verbleibt das Objekt im Arbeitsspeicher. Wenn die Verweisanzahl null erreicht, zerstört sich das Objekt selbst. Sie müssen nichts über die Verweisanzahl eines Objekts wissen. Solange Sie die Schnittstellen eines Objekts ordnungsgemäß abrufen und frei geben, hat das Objekt die entsprechende Lebensdauer.

Die ordnungsgemäße Verarbeitung der Verweiszählung ist ein wichtiger Bestandteil der COM-Programmierung. Wenn dies nicht der Fehler ist, kann dies leicht zu einem Speicherverlust oder einem Absturz führen. Einer der häufigsten Fehler, die COM-Programmierer machen, ist das Fehlschlagen der Freigabe einer Schnittstelle. In diesem Fall erreicht die Verweisanzahl nie null, und das Objekt verbleibt unbegrenzt im Arbeitsspeicher.

> [!NOTE]
> Direct3D 10 oder höher verfügt über leicht geänderte Lebensdauerregeln für Objekte. Insbesondere Objekte, die von **ID3DxxDeviceChild** abgeleitet werden, überdauern ihr übergeordnetes Gerät nie (d. h., wenn die besitzende **ID3DxxDevice** einen Refcount-Wert von 0 erreicht, sind alle untergeordneten Objekte sofort auch ungültig). Wenn Sie Set-Methoden verwenden, um Objekte an die Renderpipeline zu binden, erhöhen diese Verweise auch nicht die Verweisanzahl (d. h. sie sind schwache Verweise).  In der Praxis wird dies am besten behandelt, indem Sie sicherstellen, dass Sie alle untergeordneten Geräteobjekte vollständig frei geben, bevor Sie das Gerät frei geben.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Erhöhen und Dekrementen der Verweisanzahl

Wenn Sie einen neuen Schnittstellenzeiger erhalten, muss die Verweisanzahl durch einen Aufruf von [**IUnknown::AddRef erhöht werden.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) Ihre Anwendung muss diese Methode jedoch in der Regel nicht aufrufen. Wenn Sie einen Schnittstellenzeiger durch Aufrufen einer Objekterstellungsmethode oder durch Aufrufen von **IUnknown::QueryInterface** abrufen, erhöht das Objekt automatisch die Verweisanzahl. Wenn Sie jedoch auf andere Weise einen Schnittstellenzeiger erstellen, z. B. das Kopieren eines vorhandenen Zeigers, müssen Sie **explizit IUnknown::AddRef aufrufen.** Andernfalls kann das Objekt zerstört werden, wenn Sie den ursprünglichen Schnittstellenzeiger frei geben, auch wenn Sie möglicherweise noch die Kopie des Zeigers verwenden müssen.

Sie müssen alle Schnittstellenzeker unabhängig davon, ob Sie oder das Objekt den Verweiszähler erhöht haben, frei geben. Wenn Sie keinen Schnittstellenzeiger mehr benötigen, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, um die Verweisanzahl zu dekrementen. Eine gängige Methode besteht im Initialisieren aller Schnittstellenze zeiger auf und anschließendes Festlegen auf , `nullptr` `nullptr` wenn sie freigegeben werden. Mit dieser Konvention können Sie alle Schnittstellenzeigte in Ihrem Bereinigungscode testen. Diejenigen, die nicht aktiv sind, sind weiterhin aktiv, und Sie müssen sie `nullptr` veröffentlichen, bevor Sie die Anwendung beenden.

Das folgende Codefragment erweitert das weiter oben gezeigte Beispiel, um die Handhabung der Verweiszählung zu veranschaulichen.

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

## <a name="com-smart-pointers"></a>Intelligente COM-Zeiger

Der Code hat bisher explizit und aufgerufen, um die Verweisanzahl mithilfe ``Release`` ``AddRef`` von **IUnknown-Methoden zu** verwalten. Dieses Muster erfordert, dass der Programmierer sorgfältig daran denken muss, die Anzahl in allen möglichen Codepfaden ordnungsgemäß zu verwalten. Dies kann zu einer komplizierten Fehlerbehandlung führen, und bei aktivierter C++-Ausnahmebehandlung kann die Implementierung besonders schwierig sein. Eine bessere Lösung mit C++ ist die Verwendung eines intelligenten [Zeigers.](/cpp/cpp/smart-pointers-modern-cpp)

* **winrt::com_ptr** ist ein intelligenter Zeiger, der von den [C++/WinRT-Sprachprojektionen bereitgestellt wird.](/uwp/cpp-ref-for-winrt/com-ptr) Dies ist der empfohlene intelligente COM-Zeiger für UWP-Apps. Beachten Sie, dass C++/WinRT C++17 erfordert.

* **Microsoft::WRL::ComPtr** ist ein intelligenter Zeiger, der von der [Windows Runtime C++-Vorlagenbibliothek (WRL) bereitgestellt wird.](/cpp/cppcx/wrl/comptr-class) Diese Bibliothek ist "reines" C++, sodass sie für Windows Runtime-Anwendungen (über C++/CX oder C++/WinRT) sowie für klassische Win32-Desktopanwendungen verwendet werden kann. Dieser intelligente Zeiger funktioniert auch in älteren Versionen von Windows, die die Windows Runtime-APIs nicht unterstützen. Für Win32-Desktopanwendungen können Sie verwenden, um nur diese Klasse ein- und optional auch das ``#include <wrl/client.h>`` ``__WRL_CLASSIC_COM_STRICT__`` Präprozessorsymbol zu definieren. Weitere Informationen finden Sie unter [Com smart pointers revisited](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited)( Com smart pointers revisited ).

* **CComPtr ist** ein intelligenter Zeiger, der vom Active Template Library [(ATL) bereitgestellt wird.](/cpp/atl/reference/ccomptr-class) **Microsoft::WRL::ComPtr** ist eine neuere Version dieser Implementierung, die eine Reihe von subtilen Verwendungsproblemen behandelt, sodass die Verwendung dieses intelligenten Zeigers für neue Projekte nicht empfohlen wird. Weitere Informationen finden Sie unter Erstellen und Verwenden [von CComPtr und CComQIPtr.](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances)


## <a name="using-atl-with-directx-9"></a>Verwenden von ATL mit DirectX 9

Um die Active Template Library (ATL) mit DirectX 9 zu verwenden, müssen Sie die Schnittstellen für ATL-Kompatibilität neu definieren. Dadurch können Sie die **CComQIPtr-Klasse** ordnungsgemäß verwenden, um einen Zeiger auf eine Schnittstelle zu erhalten.

Sie werden wissen, ob Sie die Schnittstellen für ATL nicht neu definieren, da die folgende Fehlermeldung angezeigt wird.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

Das folgende Codebeispiel zeigt, wie die IDirectXFileData-Schnittstelle definiert wird.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Nachdem Sie die Schnittstelle neu definiert haben, müssen Sie die **Attach-Methode** verwenden, um die Schnittstelle an den Schnittstellenzeiger anfügen, der von **::D ct3DCreate9 zurückgegeben wird.** Wenn dies nicht der Dert ist, wird die **IDirect3D9-Schnittstelle** nicht ordnungsgemäß von der intelligenten Zeigerklasse freigegeben.

Die **CComPtr-Klasse** ruft **intern IUnknown::AddRef** für den Schnittstellenzeiger auf, wenn das Objekt erstellt wird und eine Schnittstelle der **CComPtr-Klasse zugewiesen** wird. Rufen Sie **IUnknown::AddRef nicht auf der Schnittstelle auf, die von **::D ct3DCreate9** zurückgegeben wird, um ein Offenlegungsverlust des Schnittstellenzeigers zu vermeiden.

Der folgende Code gibt die Schnittstelle ordnungsgemäß frei, ohne **IUnknown::AddRef auf aufruft.**

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Verwenden Sie den vorherigen Code. Verwenden Sie nicht den folgenden Code, der **IUnknown::AddRef** gefolgt von **IUnknown::Release** aufruft und den von **::D ct3DCreate9** hinzugefügten Verweis nicht frei gibt.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Beachten Sie, dass dies der einzige Ort in Direct3D 9 ist, an dem Sie die **Attach-Methode** auf diese Weise verwenden müssen.

Weitere Informationen zu den **Klassen CComPTR** und **CComQIPtr** finden Sie unter deren Definitionen in der `Atlbase.h` Headerdatei.
