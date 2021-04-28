---
title: Fehlerbehandlung in COM (Los geht's mit Win32 und C++)
description: Fehlerbehandlung in COM (Los geht's mit Win32 und C++)
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cf89170087469fa6ef8587fb5377e6374f6a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103918"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Fehlerbehandlung in COM (Los geht's mit Win32 und C++)

COM verwendet **HRESULT-Werte,** um den Erfolg oder Fehler eines Methoden- oder Funktionsaufrufs anzugeben. Verschiedene SDK-Header definieren verschiedene **HRESULT-Konstanten.** Ein häufiger Satz von systemweiten Codes wird in WinError.h definiert. In der folgenden Tabelle sind einige dieser systemweiten Rückgabecodes aufgeführt.



| Konstante            | Numerischer Wert | BESCHREIBUNG                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ ACCESSDENIED** | 0x80070005    | Der Zugriff wurde verweigert.                                       |
| **E \_ FAIL**         | 0x80004005    | Unbekannter Fehler.                                   |
| **E \_ INVALIDARG**   | 0x80070057    | Ungültiger Parameterwert.                             |
| **E \_ OUTOFMEMORY**  | 0x8007000E    | Nicht genügend Arbeitsspeicher.                                       |
| **\_E-ZEIGER**      | 0x80004003    | **NULL** wurde für einen Zeigerwert falsch übergeben. |
| **E \_ UNEXPECTED**   | 0x8000FFFF    | Unerwartete Bedingung.                                |
| **S \_ OK**           | 0x0           | Erfolg.                                             |
| **S \_ FALSE**        | 0x1           | Erfolg.                                             |



 

Alle Konstanten mit dem Präfix \_ "E" sind Fehlercodes. Die Konstanten **S \_ OK** und **S \_ FALSE** sind beide Erfolgscodes. Wahrscheinlich geben 99 % der COM-Methoden **S \_ OK** zurück, wenn sie erfolgreich sind, aber lassen Sie sich von dieser Tatsache nicht irreführen. Eine Methode gibt möglicherweise andere Erfolgscodes zurück. Testen Sie daher immer mithilfe des Makros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) oder [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) auf Fehler. Der folgende Beispielcode zeigt die falsche Methode und die richtige Methode, um den Erfolg eines Funktionsaufrufs zu testen.


```C++
// Wrong.
HRESULT hr = SomeFunction();
if (hr != S_OK)
{
    printf("Error!\n"); // Bad. hr might be another success code.
}

// Right.
HRESULT hr = SomeFunction();
if (FAILED(hr))
{
    printf("Error!\n"); 
}
```



Der Erfolgscode **S \_ FALSE** ist zu erwähnen. Einige Methoden verwenden **S \_ FALSE,** um ungefähr eine negative Bedingung zu bedeuten, die kein Fehler ist. Sie kann auch auf "no-op" hinweisen– die Methode war erfolgreich, hatte aber keine Auswirkungen. Beispielsweise gibt die [**CoInitializeEx-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) **S \_ FALSE** zurück, wenn Sie sie ein zweites Mal aus dem gleichen Thread aufrufen. Wenn Sie in Ihrem Code zwischen **S \_ OK** und **S \_ FALSE** unterscheiden müssen, sollten Sie den Wert direkt testen, aber trotzdem [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) oder [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) verwenden, um die verbleibenden Fälle zu behandeln, wie im folgenden Beispielcode gezeigt.


```C++
if (hr == S_FALSE)
{
    // Handle special case.
}
else if (SUCCEEDED(hr))
{
    // Handle general success case.
}
else
{
    // Handle errors.
    printf("Error!\n"); 
}
```



Einige **HRESULT-Werte** sind spezifisch für ein bestimmtes Feature oder Subsystem von Windows. Beispielsweise definiert die Direct2D-Grafik-API den Fehlercode **D2DERR \_ UNSUPPORTED \_ PIXEL \_ FORMAT**, was bedeutet, dass das Programm ein nicht unterstütztes Pixelformat verwendet hat. Die MSDN-Dokumentation enthält häufig eine Liste spezifischer Fehlercodes, die von einer Methode zurückgegeben werden können. Sie sollten diese Listen jedoch nicht als endgültig betrachten. Eine Methode kann immer einen **HRESULT-Wert** zurückgeben, der nicht in der Dokumentation aufgeführt ist. Verwenden Sie erneut die Makros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) und [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) Wenn Sie auf einen bestimmten Fehlercode testen, schließen Sie auch einen Standardfall ein.


```C++
if (hr == D2DERR_UNSUPPORTED_PIXEL_FORMAT)
{
    // Handle the specific case of an unsupported pixel format.
}
else if (FAILED(hr))
{
    // Handle other errors.
}
```



## <a name="patterns-for-error-handling"></a>Muster für die Fehlerbehandlung

In diesem Abschnitt werden einige Muster für die strukturierte Behandlung von COM-Fehlern behandelt. Jedes Muster hat Vor- und Nachteile. Bis zu einem gewissen Grad ist die Auswahl eine Frage des Vorliebes. Wenn Sie an einem vorhandenen Projekt arbeiten, verfügen sie möglicherweise bereits über Codierungsrichtlinien, die einen bestimmten Stil prokribieren. Unabhängig davon, welches Muster Sie übernehmen, befolgt robuster Code die folgenden Regeln.

-   Überprüfen Sie für jede Methode oder Funktion, die **ein HRESULT zurückgibt,** den Rückgabewert, bevor Sie fortfahren.
-   Geben Sie Ressourcen frei, nachdem sie verwendet wurden.
-   Versuchen Sie nicht, auf ungültige oder nicht initialisierte Ressourcen wie **NULL-Zeiger** zu zugreifen.
-   Versuchen Sie nicht, eine Ressource zu verwenden, nachdem Sie sie veröffentlicht haben.

Im Folgenden finden Sie vier Muster für die Fehlerbehandlung.

-   [Geschachtelte ifs](#nested-ifs)
-   [Kaskadierenden Ifs](#cascading-ifs)
-   [Jump on Fail](#jump-on-fail)
-   [Bei Fehler auslösen](#throw-on-fail)

### <a name="nested-ifs"></a>Geschachtelte ifs

Verwenden Sie nach jedem Aufruf, der **ein HRESULT zurückgibt,** eine **if-Anweisung,** um den Erfolg zu testen. Legen Sie dann den nächsten Methodenaufruf innerhalb des Bereichs der **if-Anweisung** ab. Mehr  if-Anweisungen können so tief wie nötig geschachtelt werden. In den vorherigen Codebeispielen in diesem Modul wurde dieses Muster verwendet, aber hier ist es wieder so:


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                // Use pItem (not shown). 
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    return hr;
}
```



Vorteile

-   Variablen können mit minimalem Gültigkeitsbereich deklariert werden. Beispielsweise wird *pItem erst* deklariert, wenn es verwendet wird.
-   Innerhalb jeder **if-Anweisung** sind bestimmte Invarianten true: Alle vorherigen Aufrufe sind erfolgreich, und alle erworbenen Ressourcen sind weiterhin gültig. Wenn das Programm im vorherigen Beispiel die innerste **if-Anweisung** erreicht, sind *sowohl pItem* als auch *pFileOpen* als gültig bekannt.
-   Es ist klar, wann Schnittstellenzeiger und andere Ressourcen veröffentlicht werden müssen. Sie geben eine Ressource am Ende der **if-Anweisung** frei, die unmittelbar auf den Aufruf folgt, der die Ressource erworben hat.

Nachteile

-   Bei einigen Personen ist die tiefe Schachtelung schwer zu lesen.
-   Die Fehlerbehandlung wird mit anderen Verzweigungs- und Schleifenanweisungen kombiniert. Dies kann die Verfolgung der gesamten Programmlogik erschweren.

### <a name="cascading-ifs"></a>Kaskadierende Ifs

Verwenden Sie nach jedem  Methodenaufruf eine if-Anweisung, um den Erfolg zu testen. Wenn die Methode erfolgreich ist, platzieren  Sie den nächsten Methodenaufruf im if-Block. Anstatt jedoch weitere **if-Anweisungen** zu schachteln, platzieren Sie jeden nachfolgenden [**SUCCEEDED-Test**](/windows/desktop/api/winerror/nf-winerror-succeeded) nach dem vorherigen **if-Block.** Wenn eine Methode fehlschlägt, schlagen alle verbleibenden **SUCCEEDED-Tests** einfach fehl, bis der untere Rand der Funktion erreicht ist.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }
    if (SUCCEEDED(hr))
    {
        // Use pItem (not shown).
    }

    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



In diesem Muster geben Sie Ressourcen ganz am Ende der Funktion frei. Wenn ein Fehler auftritt, sind einige Zeiger möglicherweise ungültig, wenn die Funktion beendet wird. Wenn [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für einen ungültigen Zeiger aufgerufen wird, stürzt das Programm ab (oder noch schlechter). Daher müssen Sie alle Zeiger auf **NULL** initialisieren und überprüfen, ob sie **NULL** sind, bevor Sie sie freigeben. In diesem Beispiel wird die `SafeRelease` -Funktion verwendet. Intelligente Zeiger sind ebenfalls eine gute Wahl.

Wenn Sie dieses Muster verwenden, müssen Sie mit Schleifenkonstrukten vorsichtig sein. Unterbrechen Sie innerhalb einer Schleife die Schleife, wenn ein Aufruf fehlschlägt.

Vorteile

-   Dieses Muster erstellt weniger Schachtelung als das "geschachtelte Ifs"-Muster.
-   Die allgemeine Ablaufsteuerung ist einfacher zu erkennen.
-   Ressourcen werden an einem Punkt im Code freigegeben.

Nachteile

-   Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.
-   Wenn ein Aufruf fehlschlägt, nimmt die Funktion mehrere nicht benötigte Fehlerüberprüfungen vor, anstatt die Funktion sofort zu beenden.
-   Da der Ablauf der Steuerung nach einem Fehler durch die Funktion fortgesetzt wird, müssen Sie im gesamten Funktionstext darauf achten, nicht auf ungültige Ressourcen zuzugreifen.
-   Fehler innerhalb einer Schleife erfordern einen Sonderfall.

### <a name="jump-on-fail"></a>Fehler beim Springen

Testen Sie nach jedem Methodenaufruf auf Fehler (nicht erfolgreich). Wechseln Sie bei einem Fehler zu einer Bezeichnung am unteren Rand der Funktion. Geben Sie nach der Bezeichnung, aber vor dem Beenden der Funktion Ressourcen frei.


```C++
HRESULT ShowDialog()
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->Show(NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pFileOpen->GetResult(&pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use pItem (not shown).

done:
    // Clean up.
    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
    return hr;
}
```



Vorteile

-   Die allgemeine Ablaufsteuerung ist leicht zu erkennen.
-   Wenn Sie nicht zur Bezeichnung gesprungen sind, ist an jedem Punkt im Code nach einer [**FAILED-Überprüfung**](/windows/desktop/api/winerror/nf-winerror-failed) garantiert, dass alle vorherigen Aufrufe erfolgreich waren.
-   Ressourcen werden an einer Stelle im Code freigegeben.

Nachteile

-   Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.
-   Einige Programmierer möchten **goto** nicht in ihrem Code verwenden. (Beachten Sie jedoch, dass diese Verwendung von **goto** stark strukturiert ist. Der Code springt nie außerhalb des aktuellen Funktionsaufrufs.)
-   **goto-Anweisungen** überspringen Initialisierer.

### <a name="throw-on-fail"></a>Bei Fehler auslösen

Anstatt zu einer Bezeichnung zu springen, können Sie eine Ausnahme auslösen, wenn eine Methode fehlschlägt. Dies kann zu einem idiomatischen C++-Stil führen, wenn Sie es gewohnt sind, ausnahmesicheren Code zu schreiben.


```C++
#include <comdef.h>  // Declares _com_error

inline void throw_if_fail(HRESULT hr)
{
    if (FAILED(hr))
    {
        throw _com_error(hr);
    }
}

void ShowDialog()
{
    try
    {
        CComPtr<IFileOpenDialog> pFileOpen;
        throw_if_fail(CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen)));

        throw_if_fail(pFileOpen->Show(NULL));

        CComPtr<IShellItem> pItem;
        throw_if_fail(pFileOpen->GetResult(&pItem));

        // Use pItem (not shown).
    }
    catch (_com_error err)
    {
        // Handle error.
    }
}
```



Beachten Sie, dass in diesem Beispiel die **CComPtr-Klasse** zum Verwalten von Schnittstellenzeigern verwendet wird. Wenn Ihr Code Ausnahmen auslöst, sollten Sie im Allgemeinen das RAII-Muster (Resource Acquisition is Initialization) befolgen. Das heißt, jede Ressource sollte von einem Objekt verwaltet werden, dessen Destruktor garantiert, dass die Ressource ordnungsgemäß freigegeben wird. Wenn eine Ausnahme ausgelöst wird, wird der Destruktor garantiert aufgerufen. Andernfalls kann das Programm Ressourcenverlusten.

Vorteile

-   Kompatibel mit vorhandenem Code, der die Ausnahmebehandlung verwendet.
-   Kompatibel mit C++-Bibliotheken, die Ausnahmen auslösen, z. B. die Standardvorlagenbibliothek (STL).

Nachteile

-   Erfordert, dass C++-Objekte Ressourcen wie Arbeitsspeicher oder Dateihandles verwalten.
-   Erfordert ein gutes Verständnis des Schreibens von ausnahmesicherem Code.

## <a name="next"></a>Nächste

[Modul 3. Windows-Grafiken](module-3---windows-graphics.md)

 

 
