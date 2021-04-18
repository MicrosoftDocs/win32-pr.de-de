---
title: Speicher Belegung in com
description: .
ms.assetid: b3c318d2-1273-430e-8aca-5bd5c95c138e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62227f78287f184b019eee3e498ec8a25f25a03c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338461"
---
# <a name="memory-allocation-in-com"></a>Speicher Belegung in com

Manchmal ordnet eine Methode einen Speicherpuffer auf dem Heap zu und gibt die Adresse des Puffers an den Aufrufer zurück. COM definiert ein Funktions Paar zum Zuordnen und Freigeben von Arbeitsspeicher auf dem Heap.

-   Die [**cotaskmembelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) -Funktion weist einen Speicherblock zu.
-   Die [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) -Funktion gibt einen Speicherblock frei, der mit [**cotaskmembelegc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)zugeordnet wurde.

Wir haben ein Beispiel für dieses Muster im [Dialogfeld "Öffnen" angezeigt](example--the-open-dialog-box.md):


```C++
PWSTR pszFilePath;
hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
if (SUCCEEDED(hr))
{
    // ...
    CoTaskMemFree(pszFilePath);
}
```



Die [**GetDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname) -Methode ordnet Speicher für eine Zeichenfolge zu. Intern wird von der-Methode [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) aufgerufen, um die Zeichenfolge zuzuordnen. Wenn die-Methode zurückgegeben wird, verweist *pszfilepath* auf den Speicherort des neuen Puffers. Der Aufrufer ist für das Aufrufen von [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) zuständig, um den Arbeitsspeicher freizugeben.

Warum definiert com seine eigenen Speicher Belegungs Funktionen? Ein Grund ist, eine Abstraktions Ebene über die Heap Zuweisung bereitzustellen. Andernfalls können einige Methoden **malloc** aufrufen, während andere als **New** bezeichnet werden. Dann müsste Ihr Programm in einigen Fällen **kostenlos** anrufen und in anderen Fällen **Löschen** , und die Nachverfolgung des gesamten Programms würde schnell unmöglich werden. Die com-Zuordnungs Funktionen erstellen einen einheitlichen Ansatz.

Ein weiterer Aspekt ist die Tatsache, dass com ein *binärer* Standard ist, sodass er nicht an eine bestimmte Programmiersprache gebunden ist. Daher kann com nicht auf eine sprachspezifische Form der Speicher Belegung zurückgreifen.

## <a name="next"></a>Nächste

[COM-Codierungs Methoden](com-coding-practices.md)

 

 