---
title: Abrufen der Adresse einer virtuellen Funktions Tabelle
description: Abrufen der Adresse einer virtuellen Funktions Tabelle
ms.assetid: c9e9e2df-75e6-4684-a465-6905e76b10a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c0d618e75d2c3a4fcc2550fca7cb90bd2a51d2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515728"
---
# <a name="obtaining-the-address-of-a-virtual-function-table"></a><span data-ttu-id="7486f-103">Abrufen der Adresse einer virtuellen Funktions Tabelle</span><span class="sxs-lookup"><span data-stu-id="7486f-103">Obtaining the Address of a Virtual Function Table</span></span>

<span data-ttu-id="7486f-104">In einer Anwendung, die in der Programmiersprache C geschrieben wurde, können Sie die Adresse der **iavistreamvtbl** -Struktur mithilfe der Newball-Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="7486f-104">In an application written in the C programming language, you can retrieve the address of the **IAVIStreamVtbl** structure by using the NewBall function.</span></span> <span data-ttu-id="7486f-105">Diese Funktion gibt die Adresse einer Struktur zurück, die einen Zeiger auf **iavistreamvtbl** enthält.</span><span class="sxs-lookup"><span data-stu-id="7486f-105">This function returns the address of a structure containing a pointer to **IAVIStreamVtbl**.</span></span> <span data-ttu-id="7486f-106">Die nach dem **iavistreamvtbl** -Zeiger folgenden Informationen geben Daten an, die intern von aviball verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7486f-106">Information following the **IAVIStreamVtbl** pointer specifies data used internally by AVIBall.</span></span> <span data-ttu-id="7486f-107">Der Stream-Handler kann seine eigenen Informationen nach dem **iavistreamvtbl** -Zeiger anfügen.</span><span class="sxs-lookup"><span data-stu-id="7486f-107">Your stream handler can append its own information after the **IAVIStreamVtbl** pointer.</span></span> <span data-ttu-id="7486f-108">Diese Informationen werden in nachfolgenden Aufrufen Ihres Stream-Handlers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7486f-108">This information is returned in subsequent calls to your stream handler.</span></span>


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



 

 




