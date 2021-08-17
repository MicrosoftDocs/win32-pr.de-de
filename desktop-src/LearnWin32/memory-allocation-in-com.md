---
title: Speicherzuordnung in COM
description: Speicherzuordnung in COM
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a38477f0db860cf768493417470f2da3395e814bc106cf85f975ed11ba2c0b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979980"
---
# <a name="memory-allocation-in-com"></a>Speicherzuordnung in COM

Manchmal weist eine Methode dem Heap einen Speicherpuffer zu und gibt die Adresse des Puffers an den Aufrufer zurück. COM definiert ein Funktionspaar zum Zuweisen und Frei geben von Arbeitsspeicher auf dem Heap.

-   Die [**CoTaskMemAlloc-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) weist einen Speicherblock zu.
-   Die [**CoTaskMemFree-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) gibt einen Speicherblock frei, der mit [**CoTaskMemAlloc zugeordnet wurde.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)

Ein Beispiel für dieses Muster wurde im Beispiel [des Dialogfelds Öffnen angezeigt:](example--the-open-dialog-box.md)


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Die [**GetDisplayName-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) ordnet Arbeitsspeicher für eine Zeichenfolge zu. Intern ruft die Methode [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) auf, um die Zeichenfolge zu zuordnen. Wenn die Methode zurückgegeben wird, *zeigt pszFilePath* auf den Speicherort des neuen Puffers. Der Aufrufer ist für den Aufruf von [**CoTaskMemFree verantwortlich,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher frei zu geben.

Warum definiert COM eigene Speicherzuweisungsfunktionen? Ein Grund ist die Bereitstellung einer Abstraktionsschicht über der Heapzuweisung. Andernfalls können einige Methoden **malloc aufrufen,** während andere neue **aufgerufen haben.** Dann müsste Ihr Programm in einigen Fällen  kostenlos aufrufen und **in** anderen löschen, und das Nachverfolgen würde schnell unmöglich werden. Die COM-Zuordnungsfunktionen erstellen einen einheitlichen Ansatz.

Ein weiterer Aspekt ist die Tatsache, dass COM ein *binärer* Standard ist und daher nicht an eine bestimmte Programmiersprache gebunden ist. Aus diesem Grund kann COM sich nicht auf eine sprachspezifische Form der Speicherzuweisung verlassen.

## <a name="next"></a>Nächste

[COM-Codierungsmethoden](com-coding-practices.md)

 

 
