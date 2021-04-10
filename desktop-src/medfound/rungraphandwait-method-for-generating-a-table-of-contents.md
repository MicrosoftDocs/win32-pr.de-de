---
description: Rungraphandwait-Funktion zum Erstellen eines Inhaltsverzeichnisses
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: Rungraphandwait-Funktion zum Erstellen eines Inhaltsverzeichnisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215012"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a><span data-ttu-id="7abc4-103">Rungraphandwait-Funktion zum Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="7abc4-103">RunGraphAndWait Function for Generating a Table of Contents</span></span>

<span data-ttu-id="7abc4-104">Die folgende Funktion ist eine Hilfsfunktion in einem Beispielprogramm, das unter [Automatisches Erstellen eines Inhaltsverzeichnisses](generating-a-table-of-contents-automatically.md)erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="7abc4-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="7abc4-105">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7abc4-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7abc4-106">Automatisches Erstellen eines Inhaltsverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="7abc4-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



