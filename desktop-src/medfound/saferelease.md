---
description: Saferelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: Saferelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360129"
---
# <a name="saferelease"></a><span data-ttu-id="c4190-103">Saferelease</span><span class="sxs-lookup"><span data-stu-id="c4190-103">SafeRelease</span></span>


<span data-ttu-id="c4190-104">Viele der Codebeispiele in dieser Dokumentation verwenden die folgende Funktion zum Freigeben von COM-Schnittstellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="c4190-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="c4190-105">Diese Funktion ist nicht in einem SDK-Header definiert.</span><span class="sxs-lookup"><span data-stu-id="c4190-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="c4190-106">Um diese Funktion verwenden zu können, müssen Sie Sie in Ihrem eigenen Code definieren.</span><span class="sxs-lookup"><span data-stu-id="c4190-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="c4190-107">Diese Funktion gibt den Zeiger *ppT* frei und legt ihn gleich **null** fest.</span><span class="sxs-lookup"><span data-stu-id="c4190-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="c4190-108">Eine andere Möglichkeit ist die Verwendung einer intelligenten Zeiger Klasse, z. b. **CComPtr**, die im Active Template Library (ATL) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c4190-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4190-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4190-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4190-110">Info über Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4190-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="c4190-111">**IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="c4190-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
