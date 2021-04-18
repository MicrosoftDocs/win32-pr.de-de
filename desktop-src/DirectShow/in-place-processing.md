---
description: In-Place Verarbeitung
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340083"
---
# <a name="in-place-processing"></a><span data-ttu-id="e036a-103">In-Place Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="e036a-103">In-Place Processing</span></span>

<span data-ttu-id="e036a-104">Bestimmte Daten Transformationen können durch direktes Ändern der Daten erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="e036a-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="e036a-105">Dies *wird als direkte Verarbeitung bezeichnet* .</span><span class="sxs-lookup"><span data-stu-id="e036a-105">This is called *in-place* processing.</span></span> <span data-ttu-id="e036a-106">Viele Audio-und Video Effekte können auf diese Weise ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e036a-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="e036a-107">Wenn ein DMO die direkte Verarbeitung unterstützt, wird die [**imediaobjectinplace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e036a-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="e036a-108">Die direkte Verarbeitung ist im Allgemeinen effizienter als die Verwendung separater Puffer für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e036a-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="e036a-109">(Eine wichtige Ausnahme ist, wenn sich der Puffer im Videospeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="e036a-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="e036a-110">In dieser Situation sind Lesevorgänge viel langsamer als Schreibvorgänge, sodass die direkte Verarbeitung nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="e036a-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="e036a-111">Zum Verarbeiten von Daten führt der Client einen einzigen Aufruf an die [**imediaobjectinplace::P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) -Methode anstelle von separaten Aufrufen von **ProcessInput** und **ProcessOutput** aus.</span><span class="sxs-lookup"><span data-stu-id="e036a-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="e036a-112">Die **Prozess** Methode ist synchron. die gesamte Verarbeitung erfolgt innerhalb des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="e036a-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="e036a-113">Außerdem werden bei der direkten Verarbeitung keine **imediabuffer** -Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="e036a-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="e036a-114">Die **Process** -Methode nimmt einen Zeiger direkt auf den Speicherpuffer an.</span><span class="sxs-lookup"><span data-stu-id="e036a-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="e036a-115">Ein DMO, der die direkte Verarbeitung unterstützt, muss immer noch die **imediaobject** -Schnittstelle implementieren, einschließlich der Methoden **ProcessInput** und **ProcessOutput** .</span><span class="sxs-lookup"><span data-stu-id="e036a-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="e036a-116">Der Client kann auswählen, ob die direkte Verarbeitung verwendet oder separate Puffer verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e036a-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="e036a-117">Kombinieren Sie die beiden Verarbeitungs Typen jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="e036a-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="e036a-118">Wenn Sie **Process** aufrufen, dürfen Sie **ProcessInput** oder **ProcessOutput** nicht aufrufen und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="e036a-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="e036a-119">**Effekt-Tails**</span><span class="sxs-lookup"><span data-stu-id="e036a-119">**Effect Tails**</span></span>

<span data-ttu-id="e036a-120">Ein direkter DMO erstellt möglicherweise eine zusätzliche Ausgabe, nachdem die Eingabe angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="e036a-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="e036a-121">Dies wird als *Effekt* Ende bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e036a-121">This is called an *effect tail*.</span></span> <span data-ttu-id="e036a-122">Beispielsweise wird ein Hall Effekt fortgesetzt, nachdem die Eingabe den Ruhe-</span><span class="sxs-lookup"><span data-stu-id="e036a-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="e036a-123">Wenn ein Effekt Ende vorliegt, gibt die **Process** -Methode den Wert "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e036a-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="e036a-124">Nachdem die Anwendung alle Daten verarbeitet hat, kann Sie das Effekt Ende generieren, indem leere Puffer an die **Prozess** Methode gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e036a-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e036a-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e036a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e036a-126">Direktes Hosting eines DMO</span><span class="sxs-lookup"><span data-stu-id="e036a-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



