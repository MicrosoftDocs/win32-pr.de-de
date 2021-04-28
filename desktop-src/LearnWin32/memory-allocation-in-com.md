---
title: Speicherbelegung in COM
description: Speicherbelegung in COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cb9913da55fab82f699ac05dae3998f7582224
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103888"
---
# <a name="memory-allocation-in-com"></a>Speicherbelegung in COM

Manchmal ordnet eine Methode einen Speicherpuffer auf dem Heap zu und gibt die Adresse des Puffers an den Aufrufer zurück. COM definiert ein Paar von Funktionen zum Zuordnen und Freigeben von Arbeitsspeicher auf dem Heap.

-   Die [**CoTaskMemAlloc-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) weist einen Speicherblock zu.
-   Die [**CoTaskMemFree-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) gibt einen Speicherblock frei, der mit [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)belegt wurde.

Wir haben ein Beispiel für dieses Muster im Beispiel für das [Dialogfeld Öffnen](example--the-open-dialog-box.md)gesehen:


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Die [**GetDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) belegt Arbeitsspeicher für eine Zeichenfolge. Intern ruft die Methode [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um die Zeichenfolge zuzuordnen. Wenn die Methode zurückgegeben wird, zeigt *pszFilePath* auf den Speicherort des neuen Puffers. Der Aufrufer ist für den Aufruf [**von CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) verantwortlich, um den Arbeitsspeicher freizugeben.

Warum definiert COM eigene Speicherbelegungsfunktionen? Ein Grund dafür ist die Bereitstellung einer Abstraktionsschicht über der Heapzuweisung. Andernfalls können einige Methoden **malloc** aufrufen, während andere **neue** aufgerufen haben. Dann müsste Ihr Programm in einigen Fällen **"free"** aufrufen und in anderen **löschen,** und es wäre schnell unmöglich, alles nachzuverfolgen. Die COM-Zuordnungsfunktionen erstellen einen einheitlichen Ansatz.

Ein weiterer Aspekt ist die Tatsache, dass COM ein *binärer* Standard ist und daher nicht an eine bestimmte Programmiersprache gebunden ist. Aus diesem Grund kann COM sich nicht auf eine sprachspezifische Form der Speicherbelegung verlassen.

## <a name="next"></a>Nächste

[COM-Codierungsmethoden](com-coding-practices.md)

 

 
