---
description: Ableiten von cbasepin
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Ableiten von cbasepin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344581"
---
# <a name="deriving-from-cbasepin"></a><span data-ttu-id="bdcdc-103">Ableiten von cbasepin</span><span class="sxs-lookup"><span data-stu-id="bdcdc-103">Deriving from CBasePin</span></span>

<span data-ttu-id="bdcdc-104">Zum Implementieren einer PIN mit [**cbasepin**](cbasepin.md)müssen Sie eine neue Klasse von der Basisklasse ableiten und mehrere ihrer Methoden überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-104">To implement a pin using [**CBasePin**](cbasepin.md), you must derive a new class from the base class and override several of its methods.</span></span> <span data-ttu-id="bdcdc-105">Sie müssen die folgenden Methoden überschreiben:</span><span class="sxs-lookup"><span data-stu-id="bdcdc-105">You must override the following methods:</span></span>

-   [<span data-ttu-id="bdcdc-106">**Cbasepin:: checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-106">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="bdcdc-107">**Cbasepin:: getmediatype**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-107">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="bdcdc-108">Sie müssen diese zusätzlichen Methoden wahrscheinlich außer Kraft setzen:</span><span class="sxs-lookup"><span data-stu-id="bdcdc-108">You will probably need to override these additional methods:</span></span>

-   [<span data-ttu-id="bdcdc-109">**Cbasepin:: Active**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-109">**CBasePin::Active**</span></span>](cbasepin-active.md)
-   [<span data-ttu-id="bdcdc-110">**Cbasepin:: breakconnect**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-110">**CBasePin::BreakConnect**</span></span>](cbasepin-breakconnect.md)
-   [<span data-ttu-id="bdcdc-111">**Cbasepin:: checkConnect**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-111">**CBasePin::CheckConnect**</span></span>](cbasepin-checkconnect.md)
-   [<span data-ttu-id="bdcdc-112">**Cbasepin:: completeconnect**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-112">**CBasePin::CompleteConnect**</span></span>](cbasepin-completeconnect.md)
-   [<span data-ttu-id="bdcdc-113">**Cbasepin:: EndOf Stream**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-113">**CBasePin::EndOfStream**</span></span>](cbasepin-endofstream.md)
-   [<span data-ttu-id="bdcdc-114">**Cbasepin:: inaktiv**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-114">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md)
-   [<span data-ttu-id="bdcdc-115">**Cbasepin:: notify**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-115">**CBasePin::Notify**</span></span>](cbasepin-notify.md)
-   [<span data-ttu-id="bdcdc-116">**Cbasepin:: Run**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-116">**CBasePin::Run**</span></span>](cbasepin-run.md)

<span data-ttu-id="bdcdc-117">Schließlich müssen Sie die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -und [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methoden implementieren.</span><span class="sxs-lookup"><span data-stu-id="bdcdc-117">Finally, you must must implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span>

<span data-ttu-id="bdcdc-118">Einige dieser Methoden werden in Basisklassen implementiert, die von **cbasepin** abgeleitet werden, z. b. [**cbaseingeputpin**](cbaseinputpin.md) und [**cbaseoutputpin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="bdcdc-118">Some of these methods are implemented in base classes that derive from **CBasePin**, such as [**CBaseInputPin**](cbaseinputpin.md) and [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdcdc-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdcdc-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdcdc-120">**Cbasepin**</span><span class="sxs-lookup"><span data-stu-id="bdcdc-120">**CBasePin**</span></span>](cbasepin.md)
</dt> </dl>

 

 



