---
title: Behandeln von MCI-Fehlern
description: Behandeln von MCI-Fehlern
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e2f3a9cc3e711db0d26f28c9ac7e3fd0a8c94eec96117a732f8024372bf9de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141022"
---
# <a name="handling-mci-errors"></a>Behandeln von MCI-Fehlern

Sie sollten immer den Rückgabewert der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) überprüfen. Wenn dies auf einen Fehler hinweist, können Sie [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) verwenden, um eine Textbeschreibung des Fehlers abzurufen.

Im folgenden Beispiel wird der von *dwError* angegebene MCI-Fehlercode an **mciGetErrorString** übergeben. Anschließend wird die resultierende Textfehlerbeschreibung mithilfe der [MessageBox-Funktion](/windows/win32/api/winuser/nf-winuser-messagebox) angezeigt.


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> Um einen [**mciSendCommand-Fehlerrückgabewert**](/previous-versions//dd757160(v=vs.85)) selbst zu interpretieren, maskieren Sie das Wort in hoher Reihenfolge (das Wort mit niedriger Reihenfolge enthält den Fehlercode). Wenn Sie den Fehlerrückgabewert jedoch an [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85))übergeben, müssen Sie den gesamten Doubleword-Wert übergeben.

 

 

 