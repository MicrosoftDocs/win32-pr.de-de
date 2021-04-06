---
title: Verwenden der Rückruf Methoden
description: Verwenden der Rückruf Methoden
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media-Format-SDK, Rückruf Methoden
- Windows Media-Format-SDK, Methoden, die asynchron aufgerufen werden
- Rückrufmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723416"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="5ae6f-106">Verwenden der Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="5ae6f-106">Using the Callback Methods</span></span>

<span data-ttu-id="5ae6f-107">Mehrere Schnittstellen im Windows Media Format SDK enthalten Methoden, die asynchron aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="5ae6f-108">Die meisten dieser Methoden verwenden Rückruf Funktionen, um Informationen an die steuernde Anwendung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="5ae6f-109">In den folgenden Abschnitten werden einige allgemeine Probleme im Zusammenhang mit der Verwendung von Rückruf Methoden mit dem Windows Media-Format-SDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="5ae6f-110">`Section`</span><span class="sxs-lookup"><span data-stu-id="5ae6f-110">Section</span></span>                                                                          | <span data-ttu-id="5ae6f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ae6f-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ae6f-112">Verwenden des OnStatus-Rückrufs</span><span class="sxs-lookup"><span data-stu-id="5ae6f-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="5ae6f-113">Beschreibt das Implementieren der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode, die von mehreren-Objekten verwendet wird, um den Fortschritt des SDK-Vorgangs zu informieren.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="5ae6f-114">Verwenden von Ereignissen mit asynchronen Aufrufen</span><span class="sxs-lookup"><span data-stu-id="5ae6f-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="5ae6f-115">Beschreibt ein gängiges Verfahren zum Verarbeiten von asynchronen Methoden aufrufen in einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="5ae6f-116">Verwenden des Kontext Parameters</span><span class="sxs-lookup"><span data-stu-id="5ae6f-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="5ae6f-117">Führt den *pvcontext* -Parameter ein, der von mehreren Rückrufen und deren Aufruf Methoden gemeinsam genutzt wird, und erläutert, wie er verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ae6f-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="5ae6f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ae6f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ae6f-119">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="5ae6f-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




