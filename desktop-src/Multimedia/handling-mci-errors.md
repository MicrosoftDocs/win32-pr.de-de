---
title: Behandeln von MCI-Fehlern
description: Behandeln von MCI-Fehlern
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340697"
---
# <a name="handling-mci-errors"></a>Behandeln von MCI-Fehlern

Sie sollten immer den Rückgabewert der Funktion [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) überprüfen. Wenn dies auf einen Fehler hinweist, können Sie [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) verwenden, um eine Textbeschreibung des Fehlers zu erhalten.

Im folgenden Beispiel wird der von *dwError* angegebene MCI-Fehlercode an **mcigeterrorstring** übergeben. Anschließend wird die resultierende Textfehler Beschreibung mithilfe der [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion angezeigt.


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
> Um einen [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Fehlerrückgabe Wert selbst zu interpretieren, maskieren Sie das höchst wertige Wort (das nieder wertige Wort enthält den Fehlercode). Wenn Sie den Fehlerrückgabe Wert an [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85))übergeben, müssen Sie jedoch den gesamten Double Word-Wert übergeben.

 

 

 