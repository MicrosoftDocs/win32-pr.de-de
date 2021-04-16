---
title: Verwalten der Lebensdauer eines Objekts
description: Erfahren Sie, wie Sie die adressf-und releasemethoden verwalten, um die Lebensdauer eines Objekts zu steuern.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551680"
---
# <a name="managing-the-lifetime-of-an-object"></a>Verwalten der Lebensdauer eines Objekts

Es gibt eine Regel für COM-Schnittstellen, die noch nicht erwähnt wurden. Jede COM-Schnittstelle muss direkt oder indirekt von einer Schnittstelle mit dem Namen " [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)" erben. Diese Schnittstelle bietet einige grundlegende Funktionen, die alle COM-Objekte unterstützen müssen.

Die [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle definiert drei Methoden:

-   [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
-   [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

Die [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode ermöglicht einem Programm, die Funktionen des Objekts zur Laufzeit abzufragen. Weitere Informationen dazu finden Sie im nächsten Thema, in dem [ein Objekt für eine Schnittstelle abgefragt](asking-an-object-for-an-interface.md)wird. Die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasemethoden**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) werden verwendet, um die Lebensdauer eines Objekts zu steuern. Dies ist der Betreff dieses Themas.

## <a name="reference-counting"></a>Verweis Zählung

Was ein Programm möglicherweise tut, wird zu einem bestimmten Zeitpunkt Ressourcen zuweisen und freigeben. Das Zuordnen einer Ressource ist einfach. Das wissen, wann die Ressource freigegeben werden soll, ist schwierig, insbesondere, wenn die Lebensdauer der Ressource den aktuellen Bereich überschreitet. Dieses Problem ist nicht eindeutig für com. Alle Programme, die Heap Speicher zuweisen, müssen das gleiche Problem lösen. Beispielsweise verwendet C++ automatische de-dektoren, während c# und Java Garbage Collection verwenden. COM verwendet einen Ansatz namens *Verweis Zählung*.

Jedes COM-Objekt behält eine interne Anzahl bei. Dies wird als Verweis Zähler bezeichnet. Der Verweis Zähler verfolgt, wie viele Verweise auf das Objekt zurzeit aktiv sind. Wenn die Anzahl der Verweise auf Null sinkt, löscht das Objekt sich selbst. Der letzte Teil sollte sich wiederholen: das Objekt löscht sich selbst. Das Programm löscht das Objekt nie explizit.

Im folgenden sind die Regeln für die Verweis Zählung aufgeführt:

-   Wenn das Objekt erstmalig erstellt wird, ist der Verweis Zähler 1. An diesem Punkt verfügt das Programm über einen einzelnen Zeiger auf das-Objekt.
-   Das Programm kann einen neuen Verweis erstellen, indem der Zeiger dupliziert (kopiert) wird. Wenn Sie den Zeiger kopieren, müssen Sie die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -Methode des Objekts aufzurufen. Diese Methode erhöht den Verweis Zähler um 1.
-   Wenn Sie mit der Verwendung eines Zeigers auf das-Objekt fertig sind, müssen Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)abrufen. Die **releasemethode** verringert den Verweis Zähler um 1. Außerdem wird der Zeiger für ungültig erklärt. Verwenden Sie den Zeiger nicht erneut, nachdem Sie **Release** aufgerufen haben. (Wenn Sie über andere Zeiger auf dasselbe Objekt verfügen, können Sie diese Zeiger weiterhin verwenden.)
-   Wenn Sie [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) mit jedem Zeiger aufgerufen haben, erreicht der Objekt Verweis Zähler des Objekts 0 (null), und das Objekt löscht sich selbst.

Im folgenden Diagramm wird ein einfacher, aber typischer Fall angezeigt.

![Diagramm, das einen einfachen Fall der Verweis Zählung anzeigt.](images/com04.png)

Das Programm erstellt ein-Objekt und speichert einen Zeiger (*p*) für das-Objekt. An diesem Punkt ist der Verweis Zähler 1. Wenn das Programm mit dem-Zeiger fertig ist, wird [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)aufgerufen. Der Verweis Zähler wird auf 0 (null) dekrementiert, und das Objekt löscht sich selbst. *P* ist nun ungültig. Es ist ein Fehler, *p* für weitere Methodenaufrufe zu verwenden.

Das nächste Diagramm zeigt ein komplexeres Beispiel.

![Darstellung der Verweis Zählung](images/com05.png)

Hier erstellt das Programm ein Objekt und speichert den Zeiger *p* wie zuvor. Als nächstes kopiert das Programm *p* in eine neue Variable, *f*. An diesem Punkt muss das Programm die [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) anrufen, um den Verweis Zähler zu erhöhen. Der Verweis Zähler ist jetzt 2, und es gibt zwei gültige Zeiger auf das-Objekt. Nehmen Sie nun an, dass das Programm die Verwendung von *p* beendet hat. Das Programm ruft [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)auf, der Verweis Zähler wird auf 1 und *p* nicht mehr gültig. *Q* ist jedoch weiterhin gültig. Später wird das Programm mit *q* beendet. Daher wird **Release** erneut aufgerufen. Der Verweis Zähler wird auf 0 (null) gesetzt, und das Objekt löscht sich selbst.

Vielleicht Fragen Sie sich, warum das Programm *p* kopieren würde. Es gibt zwei Hauptgründe: Erstens können Sie den Zeiger in einer Datenstruktur speichern, z. b. in einer Liste. Zweitens können Sie den Zeiger über den aktuellen Gültigkeitsbereich der ursprünglichen Variablen hinaus behalten. Daher müssen Sie Sie in eine neue Variable mit größerem Gültigkeitsbereich kopieren.

Ein Vorteil der Verweis Zählung besteht darin, dass Sie Zeiger in verschiedenen Code Abschnitten freigeben können, ohne dass die verschiedenen Codepfade zum Löschen des Objekts koordiniert werden. Stattdessen ruft jeder Codepfad nur [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, wenn dieser Codepfad mithilfe des-Objekts durchgeführt wird. Das Objekt behandelt das Löschen selbst zur richtigen Zeit.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Code aus dem [Dialogfeld "Öffnen" angezeigt](example--the-open-dialog-box.md) .

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

Die Verweis Zählung tritt an zwei Stellen in diesem Code auf. Wenn das Programm das allgemeine Element Dialogfeld Objekt erstellt, muss es zuerst [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf dem *pfileopen* -Zeiger aufzurufen.

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

Zweitens: Wenn die [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) -Methode einen Zeiger auf die [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) -Schnittstelle zurückgibt, muss das Programm [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf dem *pitem* -Zeiger aufrufen.

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

Beachten Sie, dass in beiden Fällen der [**releasebefehl**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) der letzte Vorgang ist, der auftritt, bevor der Zeiger den Gültigkeitsbereich verlässt. Beachten Sie auch, dass **Release** erst aufgerufen wird, nachdem Sie das **HRESULT** auf Erfolg getestet haben. Wenn z. b. beim Aufrufen von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ein Fehler auftritt, ist der *pfileopen* -Zeiger ungültig. Daher ist es ein Fehler, **Release** auf dem Zeiger aufzurufen.

## <a name="next"></a>Nächste

[Anfordern eines Objekts für eine Schnittstelle](asking-an-object-for-an-interface.md)