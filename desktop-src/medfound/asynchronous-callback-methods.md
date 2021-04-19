---
description: Asynchrone Rückruf Methoden
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Asynchrone Rückruf Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346470"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="d0bf0-103">Asynchrone Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="d0bf0-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="d0bf0-104">Media Foundation bietet eine konsistente Methode zum Implementieren von asynchronen Methoden mithilfe einer Rückruf Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="d0bf0-105">In diesem Abschnitt wird beschrieben, wie die Rückruf Schnittstelle implementiert wird und wie asynchrone Methoden geschrieben werden, die diese Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="d0bf0-106">Es enthält die folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-106">It contains the following topics.</span></span>



| <span data-ttu-id="d0bf0-107">Thema</span><span class="sxs-lookup"><span data-stu-id="d0bf0-107">Topic</span></span>                                                                                | <span data-ttu-id="d0bf0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0bf0-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0bf0-109">Aufrufen von asynchronen Methoden</span><span class="sxs-lookup"><span data-stu-id="d0bf0-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="d0bf0-110">Vorgehensweise beim Abrufen von asynchronen Methoden in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="d0bf0-111">Implementieren des asynchronen Rückrufs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="d0bf0-112">Implementierung der Rückruf Methode in der [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="d0bf0-113">Unterstützen mehrerer Rückrufe</span><span class="sxs-lookup"><span data-stu-id="d0bf0-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="d0bf0-114">Unterstützung mehrerer Rückrufe innerhalb derselben C++-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="d0bf0-115">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="d0bf0-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="d0bf0-116">Arbeits Warteschlangen stellen eine effiziente Möglichkeit dar, asynchrone Vorgänge in einem anderen Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="d0bf0-117">Schreiben einer asynchronen Methode</span><span class="sxs-lookup"><span data-stu-id="d0bf0-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="d0bf0-118">Vorgehensweise beim Implementieren von asynchronen Methoden in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="d0bf0-119">Benutzerdefinierte asynchrone Ergebnis Objekte</span><span class="sxs-lookup"><span data-stu-id="d0bf0-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="d0bf0-120">Bereitstellen einer benutzerdefinierten Implementierung der [**imfasynkresult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d0bf0-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d0bf0-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0bf0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0bf0-122">**Imfasynccallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="d0bf0-123">**Imfasynkresult-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d0bf0-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="d0bf0-124">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="d0bf0-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



