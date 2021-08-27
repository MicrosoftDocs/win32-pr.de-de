---
title: Abrufen der Adresse einer virtuellen Funktionstabelle
description: Abrufen der Adresse einer virtuellen Funktionstabelle
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a0fbf941114cfff2b930ed329f7a35962b9ef07158fd5fda16a19a73c0f692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038430"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a>Abrufen der Adresse einer virtuellen Funktionstabelle

In einer Anwendung, die in der Programmiersprache C geschrieben wurde, können Sie die Adresse der **IAVIStreamVtbl-Struktur** mithilfe der NewBall-Funktion abrufen. Diese Funktion gibt die Adresse einer -Struktur zurück, die einen Zeiger auf **IAVIStreamVtbl** enthält. Informationen, die auf den **IAVIStreamVtbl-Zeiger** folgen, geben intern von AVIBall verwendete Daten an. Ihr Streamhandler kann nach dem **IAVIStreamVtbl-Zeiger** eigene Informationen anfügen. Diese Informationen werden in nachfolgenden Aufrufen des Streamhandlers zurückgegeben.


```C++
PAVISTREAM WINAPI NewBall(VOID) 
{ 
    PAVIBALL pball; 
    pball = (PAVIBALL) GlobalAllocPtr(GHND, sizeof(AVIBALL)); 
    if (!pball) 
        return 0; 
    pball->lpvtbl = &AVIBallHandler; 
    pball->lpvtbl->Create((PAVISTREAM) pball, 0, 0); 
    return (PAVISTREAM) pball; 
} 
```



 

 




