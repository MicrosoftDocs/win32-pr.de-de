---
title: Fehlerbehandlung in com (Get Started with Win32 and C++)
description: .
ms.assetid: 022ca652-59d2-4513-9d73-1c6d8688c478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505f8cfe6867db07da77616e6a94fdc257e32f3e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341978"
---
# <a name="error-handling-in-com-get-started-with-win32-and-c"></a>Fehlerbehandlung in com (Get Started with Win32 and C++)

COM verwendet **HRESULT** -Werte, um den Erfolg oder Misserfolg einer Methode oder eines Funktions Aufrufes anzuzeigen. Verschiedene SDK-Header definieren verschiedene **HRESULT** -Konstanten. Ein allgemeiner Satz von systemweiten Codes wird in WinError. h definiert. In der folgenden Tabelle sind einige dieser systemweiten Rückgabecodes aufgeführt.



| Konstante            | Numerischer Wert | BESCHREIBUNG                                          |
|---------------------|---------------|------------------------------------------------------|
| **E \_ AccessDenied** | 0x80070005    | Zugriff verweigert.                                       |
| **E \_ fehlschlagen**         | 0x80004005    | Unbekannter Fehler.                                   |
| **E \_ invalidArg**   | 0x80070057    | Ungültiger Parameterwert.                             |
| **E \_ outo-Memory**  | 0x8007000E    | Nicht genügend Arbeitsspeicher.                                       |
| **E- \_ Zeiger**      | 0x80004003    | **Null** wurde für einen Zeiger Wert falsch übermittelt. |
| **E \_ unerwartet**   | 0x8000FFFF    | Unerwartete Bedingung.                                |
| **S \_ OK**           | 0x0           | Erfolg.                                             |
| **S \_ false**        | 0x1           | Erfolg.                                             |



 

Alle Konstanten mit dem Präfix "E \_ " sind Fehlercodes. Die Konstanten **s \_ OK** und **S \_ false** sind beide Erfolgs Codes. 99% der com-Methoden geben bei erfolgreicher Ausführung von "S" den Wert " **\_ OK** " aus. Eine Methode gibt möglicherweise andere Erfolgs Codes zurück. Testen Sie daher immer mit [**dem Makro**](/windows/desktop/api/winerror/nf-winerror-failed) [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) oder Fehler. Der folgende Beispielcode zeigt die falsche Methode und die richtige Methode zum Testen auf den Erfolg eines Funktions Aufrufes.


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



Die Erfolgs Codes **' \_ false** ' sollten erwähnt werden. Einige Methoden verwenden " **S \_ false** ", um ungefähr eine negative Bedingung zu verwenden, die kein Fehler ist. Es kann auch ein "No-op"-– die Methode war erfolgreich, aber hat keine Auswirkung. Beispielsweise gibt die [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion **S \_ false** zurück, wenn Sie Sie ein zweites Mal aus demselben Thread aufrufen. Wenn Sie in Ihrem Code zwischen **S \_ OK** und **s \_ false** unterscheiden müssen, sollten Sie den Wert direkt testen, aber dennoch " [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) " [**oder "**](/windows/desktop/api/winerror/nf-winerror-succeeded) failed" verwenden, um die restlichen Fälle zu behandeln, wie im folgenden Beispielcode gezeigt.


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



Einige **HRESULT** -Werte sind spezifisch für eine bestimmte Funktion oder ein bestimmtes Subsystem von Windows. Beispielsweise wird durch die Direct2D-Grafik-API der Fehlercode **D2DERR \_ nicht unterstütztes \_ Pixel \_ Format** definiert, was bedeutet, dass das Programm ein nicht unterstütztes Pixel Format verwendet hat. Die MSDN-Dokumentation enthält häufig eine Liste mit spezifischen Fehlercodes, die von einer Methode zurückgegeben werden können. Sie sollten diese Listen jedoch nicht als definitiv in Erwägung gezogen. Eine Methode kann immer einen **HRESULT** -Wert zurückgeben, der nicht in der Dokumentation aufgeführt ist. Verwenden Sie erneut die Makros [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) und [**failed**](/windows/desktop/api/winerror/nf-winerror-failed) . Wenn Sie auf einen bestimmten Fehlercode testen, sollten Sie auch einen Standardfall einschließen.


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

In diesem Abschnitt werden einige Muster zur Behandlung von com-Fehlern auf strukturierte Weise erläutert. Jedes Muster hat vor-und Nachteile. In gewissem Umfang ist die Wahl eine Frage des Geschmacks. Wenn Sie an einem vorhandenen Projekt arbeiten, verfügen Sie möglicherweise bereits über Codierungs Richtlinien, die einen bestimmten Stil proschreiben. Unabhängig davon, welches Muster Sie annehmen, befolgt robuster Code die folgenden Regeln.

-   Überprüfen Sie für jede Methode oder Funktion, die ein **HRESULT** zurückgibt, den Rückgabewert, bevor Sie fortfahren.
-   Freigeben von Ressourcen nach ihrer Verwendung.
-   Versuchen Sie nicht, auf ungültige oder nicht initialisierte Ressourcen wie z. b. **null** -Zeiger zuzugreifen.
-   Versuchen Sie nicht, eine Ressource zu verwenden, nachdem Sie Sie freigegeben haben.

Mit diesen Regeln sind die folgenden vier Muster zum Behandeln von Fehlern zu beachten.

-   [Netsted IFS](#nested-ifs)
-   [Kaskadierende IFS](#cascading-ifs)
-   [Springen bei Fehlschlagen](#jump-on-fail)
-   [Auslösen bei Fehlschlagen](#throw-on-fail)

### <a name="nested-ifs"></a>Netsted IFS

Verwenden Sie nach jedem Rückruf, der ein **HRESULT** zurückgibt, eine **if** -Anweisung, um den Erfolg zu testen. Fügen Sie anschließend den nächsten Methoden aufrufim Gültigkeitsbereich der **if** -Anweisung ein. Weitere **if** -Anweisungen können bei Bedarf beliebig geschachtelt werden. Die vorherigen Codebeispiele in diesem Modul haben dieses Muster verwendet, aber hier ist es noch einmal:


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

-   Variablen können mit minimalem Gültigkeitsbereich deklariert werden. Beispielsweise wird *pitem* erst deklariert, wenn es verwendet wird.
-   In jeder **if** -Anweisung haben bestimmte invarianten den Wert "true": alle vorherigen Aufrufe waren erfolgreich, und alle erhaltenen Ressourcen sind weiterhin gültig. Wenn das Programm im vorherigen Beispiel die innerste **if** -Anweisung erreicht, sind sowohl *pitem* als auch *pfileopen* als gültig bekannt.
-   Es ist klar, wann Schnittstellen Zeiger und andere Ressourcen freigegeben werden. Sie geben eine Ressource am Ende der **if** -Anweisung frei, die direkt auf den-Rückruf folgt, der die Ressource abgerufen hat.

Nachteile

-   Einige Leute finden die Tiefe Schachtelung schwer lesbar.
-   Die Fehlerbehandlung ist mit anderen Verzweigungs-und Schleifen Anweisungen gemischt. Dadurch kann die gesamte Programmlogik schwerer befolgt werden.

### <a name="cascading-ifs"></a>Kaskadierende IFS

Verwenden Sie nach jedem Methoden Aufrufes eine **if** -Anweisung, um den Erfolg zu testen. Wenn die Methode erfolgreich ist, platzieren Sie den nächsten Methoden Aufrufvorgang innerhalb des **if** -Blocks. Anstatt weitere **if** -Anweisungen zu schachteln, platzieren Sie jeden [**nachfolgenden**](/windows/desktop/api/winerror/nf-winerror-succeeded) erfolgreichen Test nach dem vorherigen **if** -Block. Wenn eine Methode fehlschlägt, schlagen alle **verbleibenden** erfolgreichen Tests einfach fehl, bis das Ende der Funktion erreicht ist.


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



In diesem Muster veröffentlichen Sie Ressourcen am Ende der Funktion. Wenn ein Fehler auftritt, sind einige Zeiger möglicherweise ungültig, wenn die Funktion beendet wird. Wenn Sie die [**Freigabe**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf einem ungültigen Zeiger aufrufen, stürzt das Programm ab (oder schlimmer), sodass Sie alle Zeiger auf **null** initialisieren und prüfen müssen, ob Sie **null** sind, bevor Sie Sie freigeben. In diesem Beispiel wird die- `SafeRelease` Funktion verwendet. intelligente Zeiger sind ebenfalls eine gute Wahl.

Wenn Sie dieses Muster verwenden, müssen Sie mit Schleifen Konstrukten bedacht werden. Brechen Sie in einer Schleife die Schleife ab, wenn ein beliebiger Rückruf fehlschlägt.

Vorteile

-   Dieses Muster erstellt weniger Schachtelung als das "Nested IFS"-Muster.
-   Die allgemeine Ablauf Steuerung ist leichter zu erkennen.
-   Ressourcen werden an einem Punkt im Code freigegeben.

Nachteile

-   Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.
-   Wenn ein-Befehl fehlschlägt, führt die Funktion mehrere nicht benötigte Fehlerüberprüfungen aus, anstatt die Funktion sofort zu beenden.
-   Da der Ablauf der Steuerung nach einem Fehler durch die Funktion weitergeleitet wird, müssen Sie im gesamten Text der Funktion darauf achten, dass Sie nicht auf ungültige Ressourcen zugreifen können.
-   Fehler in einer Schleife erfordern einen Sonderfall.

### <a name="jump-on-fail"></a>Springen bei Fehlschlagen

Prüfen Sie nach jedem Methoden Aufrufversuch, dass ein Fehler auftritt (nicht erfolgreich). Springen Sie bei einem Fehler zu einer Bezeichnung am Ende der Funktion. Geben Sie nach der Bezeichnung, aber vor dem Beenden der Funktion Ressourcen frei.


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

-   Die allgemeine Ablauf Steuerung ist leicht zu erkennen.
-   An jedem Punkt im Code nach einer [**fehlgeschlagenen**](/windows/desktop/api/winerror/nf-winerror-failed) Überprüfung ist sichergestellt, dass alle vorherigen Aufrufe erfolgreich waren, wenn Sie nicht auf die Bezeichnung gesprungen sind.
-   Ressourcen werden an einem Ort im Code freigegeben.

Nachteile

-   Alle Variablen müssen am Anfang der Funktion deklariert und initialisiert werden.
-   Einige Programmierer möchten **goto** nicht in Ihrem Code verwenden. (Es sollte jedoch beachtet werden, dass diese Verwendung von **goto** sehr strukturiert ist. der Code springt nie außerhalb des aktuellen Funktions Aufrufes.)
-   **goto** -Anweisungen überspringen Initialisierer.

### <a name="throw-on-fail"></a>Auslösen bei Fehlschlagen

Anstatt zu einer Bezeichnung zu springen, können Sie eine Ausnahme auslösen, wenn eine Methode fehlschlägt. Dies kann zu einem eher idiomatischen Stil von C++ führen, wenn Sie zum Schreiben von Ausnahme sicherem Code verwendet werden.


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



Beachten Sie, dass in diesem Beispiel die **CComPtr** -Klasse zum Verwalten von Schnittstellen Zeigern verwendet wird. Wenn Ihr Code Ausnahmen auslöst, sollten Sie im Allgemeinen das Muster RAII (Resource Acquisition Is Initialization) befolgen. Das heißt, jede Ressource sollte von einem Objekt verwaltet werden, dessen Dekonstruktor gewährleistet, dass die Ressource ordnungsgemäß freigegeben wird. Wenn eine Ausnahme ausgelöst wird, wird sichergestellt, dass der Dekonstruktor aufgerufen wird. Andernfalls könnte das Programmressourcen nicht mehr unterliegen.

Vorteile

-   Kompatibel mit vorhandenem Code, der die Ausnahmebehandlung verwendet.
-   Kompatibel mit C++-Bibliotheken, die Ausnahmen auslösen, wie z. b. die Standard Vorlagen Bibliothek (STL).

Nachteile

-   Erfordert C++-Objekte, um Ressourcen wie Arbeitsspeicher oder Datei Handles zu verwalten.
-   Erfordert ein gutes Verständnis für das Schreiben von Ausnahme sicherem Code.

## <a name="next"></a>Nächste

[Modul 3. Windows-Grafiken](module-3---windows-graphics.md)

 

 
