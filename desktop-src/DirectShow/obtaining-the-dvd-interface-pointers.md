---
description: Abrufen der DVD-Schnittstellen Zeiger
ms.assetid: 3d9315fc-dcfb-483a-9437-55c440813dc2
title: Abrufen der DVD-Schnittstellen Zeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24825b2d24ffae70e3def131e8aa522a987c11d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345986"
---
# <a name="obtaining-the-dvd-interface-pointers"></a><span data-ttu-id="7def4-103">Abrufen der DVD-Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="7def4-103">Obtaining the DVD Interface Pointers</span></span>

<span data-ttu-id="7def4-104">Nachdem das Filter Diagramm erstellt wurde, kann die Anwendung die erforderlichen Zeiger zum Steuern des DVD-Navigators, des Filter-Graph-Managers und des Videofensters abrufen.</span><span class="sxs-lookup"><span data-stu-id="7def4-104">After the filter graph is built, your application can obtain the pointers it needs to control the DVD Navigator, the Filter Graph Manager, and the video window.</span></span> <span data-ttu-id="7def4-105">Die grundlegenden Schritte, mit Fehlerüberprüfung und anderem Code, der aus Gründen der Einfachheit ausgelassen wird, sind im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7def4-105">The basic steps, with error-checking and other code left out for simplicity, are illustrated in the following code example.</span></span> <span data-ttu-id="7def4-106">Den gesamten Code finden Sie in der DVD-Beispielanwendung in der cdvdcore:: buildgraph-Methode.</span><span class="sxs-lookup"><span data-stu-id="7def4-106">The complete code is found in the DVD Sample application in the CDvdCore::BuildGraph method.</span></span> <span data-ttu-id="7def4-107">(Weitere Informationen finden Sie unter [DirectShow-Beispiele](directshow-samples.md).)</span><span class="sxs-lookup"><span data-stu-id="7def4-107">(For more information, see [DirectShow Samples](directshow-samples.md).)</span></span>


```C++
// Create an instance of the DVD Graph Builder object.
HRESULT hr;
hr = CoCreateInstance(CLSID_DvdGraphBuilder,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDvdGraphBuilder,
                          reinterpret_cast<void**>(&m_pIDvdGB));

// Build the DVD filter graph.
AM_DVD_RENDERSTATUS buildStatus;
hr = m_pIDvdGB->RenderDvdVideoVolume(pszwDiscPath, m_dwRenderFlags, &buildStatus);

// Get the pointers to the DVD Navigator interfaces.
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdInfo2, reinterpret_cast<void**>(&m_pIDvdI2));
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdControl2, reinterpret_cast<void**>(&m_pIDvdC2));
   ...    
// Get a pointer to the filter graph manager.
hr = m_pDvdGB->GetFiltergraph(&m_pGraph);
...   
// Use the graph pointer to get a pointer to IMediaControl,
// for controlling the filter graph as a whole.
hr = m_pGraph->QueryInterface(IID_IMediaControl, reinterpret_cast<void**>(&m_pIMC));
...   
// Get a pointer to IMediaEventEx,
// used for handling DVD and other filter graph events.
hr = m_pGraph->QueryInterface(IID_IMediaEventEx, reinterpret_cast<void**>(&m_pME)); 
...                
// Use the graph builder pointer again to get the IVideoWindow interface,
// to set the window style and message-handling behavior of the video renderer filter.
hr = m_pIDvdGB->GetDvdInterface(IID_IVideoWindow, reinterpret_cast<void**>(&m_pIVW));
  
hr = m_pDvdGB->GetDvdInterface(IID_IAMLine21Decoder, reinterpret_cast<void**>(&pL21Dec));
```



## <a name="related-topics"></a><span data-ttu-id="7def4-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7def4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7def4-109">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7def4-109">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



