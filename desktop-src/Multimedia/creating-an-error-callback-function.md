---
title: Erstellen einer Fehler Rückruffunktion
description: Erstellen einer Fehler Rückruffunktion
ms.assetid: a489ec94-c566-44b1-aa93-9b43f23de744
keywords:
- capsetcallbackonerror-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac37c0e12b8f92520c4445c4c5ba3361974d836
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710458"
---
# <a name="creating-an-error-callback-function"></a>Erstellen einer Fehler Rückruffunktion

Das folgende Beispiel ist eine einfache Fehler Rückruffunktion. Registrieren Sie diesen Rückruf mithilfe des [**capsetcallbackonerror**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) -Makros.


```
TCHAR gachBuffer[100]; // Global buffer.

// ErrorCallbackProc: error callback function. 
// hWnd:              capture window handle. 
// nErrID:            error code for the encountered error. 
// lpErrorText:       error text string for the encountered error. 
// 
LRESULT PASCAL ErrorCallbackProc(HWND hWnd, int nErrID,
    LPTSTR lpErrorText) 
{ 
 
    if (!hWnd) 
        return FALSE; 
 
    if (nErrID == 0)            // Starting a new major function. 
        return TRUE;            // Clear out old errors. 
 
    // Show the error identifier and text. 
    _stprintf_s(gachBuffer, TEXT("Error# %d"), nErrID); 
 
    MessageBox(hWnd, lpErrorText, gachBuffer, 
        MB_OK | MB_ICONEXCLAMATION); 
 
    return (LRESULT) TRUE; 
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




