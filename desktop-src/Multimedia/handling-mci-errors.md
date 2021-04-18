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
# <a name="handling-mci-errors"></a><span data-ttu-id="e9172-104">Behandeln von MCI-Fehlern</span><span class="sxs-lookup"><span data-stu-id="e9172-104">Handling MCI Errors</span></span>

<span data-ttu-id="e9172-105">Sie sollten immer den Rückgabewert der Funktion [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e9172-105">You should always check the return value of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="e9172-106">Wenn dies auf einen Fehler hinweist, können Sie [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85)) verwenden, um eine Textbeschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e9172-106">If it indicates an error, you can use [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) to get a textual description of the error.</span></span>

<span data-ttu-id="e9172-107">Im folgenden Beispiel wird der von *dwError* angegebene MCI-Fehlercode an **mcigeterrorstring** übergeben. Anschließend wird die resultierende Textfehler Beschreibung mithilfe der [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9172-107">The following example passes the MCI error code specified by *dwError* to **mciGetErrorString**, and then displays the resulting textual error description using the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>


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
> <span data-ttu-id="e9172-108">Um einen [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Fehlerrückgabe Wert selbst zu interpretieren, maskieren Sie das höchst wertige Wort (das nieder wertige Wort enthält den Fehlercode).</span><span class="sxs-lookup"><span data-stu-id="e9172-108">To interpret an [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) error return value yourself, mask the high-order word (the low-order word contains the error code).</span></span> <span data-ttu-id="e9172-109">Wenn Sie den Fehlerrückgabe Wert an [**mcigeterrorstring**](/previous-versions//dd757158(v=vs.85))übergeben, müssen Sie jedoch den gesamten Double Word-Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="e9172-109">If you pass the error return value to [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), however, you must pass the entire doubleword value.</span></span>

 

 

 