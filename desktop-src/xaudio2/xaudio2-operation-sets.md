---
description: In dieser Übersicht werden mehrere XAudio2-Methoden eingeführt, die Sie als Teil eines Vorgangs Satzes aufzurufen können.
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: XAudio2-Vorgangs Sätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218553"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="1b338-103">XAudio2-Vorgangs Sätze</span><span class="sxs-lookup"><span data-stu-id="1b338-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="1b338-104">In dieser Übersicht werden mehrere XAudio2-Methoden eingeführt, die Sie als Teil eines Vorgangs Satzes aufzurufen können.</span><span class="sxs-lookup"><span data-stu-id="1b338-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="1b338-105">Mehrere XAudio2-Methoden verwenden das *operationset* -Argument, das es Ihnen ermöglicht, als Teil einer verzögerten Gruppe aufgerufen zu werden.</span><span class="sxs-lookup"><span data-stu-id="1b338-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="1b338-106">Zu einem bestimmten Zeitpunkt können Sie einen vollständigen Satz von Änderungen gleichzeitig anwenden, indem Sie die Funktion [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem *operationset* -Bezeichner für diese Gruppe aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1b338-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="1b338-107">Der Bezeichner ist eine beliebige Zahl.</span><span class="sxs-lookup"><span data-stu-id="1b338-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="1b338-108">Dadurch können separate Teile des Client Codes getrennte atomarische Änderungen auf das Diagramm anwenden, ohne dass Konflikte auftreten.</span><span class="sxs-lookup"><span data-stu-id="1b338-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="1b338-109">Die empfohlene Vorgehensweise besteht darin, dass der Client immer dann einen globalen Wert erhöht, wenn er einen eindeutigen, neuen *operationsetbezeichner* generieren muss.</span><span class="sxs-lookup"><span data-stu-id="1b338-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="1b338-110">Ein Satz von Änderungen am Diagramm, das atomarisch angewendet wird, ist garantiert ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="1b338-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="1b338-111">Beispielsweise werden die Stimmen synchron gestartet.</span><span class="sxs-lookup"><span data-stu-id="1b338-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="1b338-112">Wenn Sie *operationset* auf XAUDIO2 \_ Commit now festgelegt \_ haben, wird die Änderung sofort angewendet.</span><span class="sxs-lookup"><span data-stu-id="1b338-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="1b338-113">Sie tritt in Kraft, wenn der erste Audioverarbeitungs Durchlauf nach dem Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b338-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="1b338-114">Wenn Sie [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit XAUDIO2 \_ Commit all aufzurufen \_ , werden Änderungen an allen ausstehenden Vorgängen durchgeführt, unabhängig von Ihrer *operationsetkennung* .</span><span class="sxs-lookup"><span data-stu-id="1b338-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="1b338-115">Bestimmte Methoden treten sofort in Kraft, wenn Sie von einem XAudio2-Rückruf mit einem *operationset* von XAudio2 \_ Commit now aufgerufen werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1b338-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="1b338-116">Alle anderen Methoden, die ein *operationset* -Argument annehmen, werden erst nach dem Aufrufen der-Methode (bei Aufruf mit XAUDIO2 \_ Commit \_ ) oder nach dem Aufrufen von [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem gleichen *operationset* wirksam.</span><span class="sxs-lookup"><span data-stu-id="1b338-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="1b338-117">Aus diesem Grund werden bestimmte Methodenaufrufe möglicherweise nicht immer in derselben Reihenfolge ausgeführt, in der Sie aufgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="1b338-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="1b338-118">Alle ausstehenden Vorgänge werden atomisch ausgeführt, wenn [**IXAudio2:: stopengine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1b338-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="1b338-119">Alle Methoden, die aufgerufen werden, während die Engine angehalten wird, treten unabhängig vom bereitgestellten *operationsetwert* sofort in Kraft.</span><span class="sxs-lookup"><span data-stu-id="1b338-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="1b338-120">Wenn Sie die Engine neu starten, kehrt XAudio2 in den asynchronen Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="1b338-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="1b338-121">Einfache Szenarien, in denen Vorgangs Sätze nützlich sind, sind die folgenden Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1b338-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="1b338-122">Gleichzeitiges Starten mehrerer Stimmen.</span><span class="sxs-lookup"><span data-stu-id="1b338-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="1b338-123">Gleichzeitiges Senden eines Puffers an eine Stimme, Festlegen der sprach Parameter und Starten der Stimme.</span><span class="sxs-lookup"><span data-stu-id="1b338-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="1b338-124">Eine umfangreiche Änderung des Diagramms, z. b. das Verbinden aller Quell stimmen mit einer neuen Teil Mischungs Sprache.</span><span class="sxs-lookup"><span data-stu-id="1b338-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="1b338-125">Weitere Informationen finden Sie unter Gewusst [wie: Gruppieren von Audiomethoden als Vorgangs Satz](how-to--group-audio-methods-as-an-operation-set.md) für ein Beispiel für die Verwendung eines Vorgangs Satzes.</span><span class="sxs-lookup"><span data-stu-id="1b338-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="1b338-126">Vorgangs Satz Methoden</span><span class="sxs-lookup"><span data-stu-id="1b338-126">Operation Set Methods</span></span>

<span data-ttu-id="1b338-127">Sie können die folgenden Methoden als Teil eines Vorgangs Satzes aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b338-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="1b338-128">**IXAudio2SourceVoice:: exitloop**</span><span class="sxs-lookup"><span data-stu-id="1b338-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="1b338-129">**IXAudio2Voice:: setfilterparameters**</span><span class="sxs-lookup"><span data-stu-id="1b338-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="1b338-130">**IXAudio2SourceVoice:: setfrequendcyratio**</span><span class="sxs-lookup"><span data-stu-id="1b338-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="1b338-131">**IXAudio2Voice::D isableeffect**</span><span class="sxs-lookup"><span data-stu-id="1b338-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="1b338-132">**IXAudio2Voice:: enableeffect**</span><span class="sxs-lookup"><span data-stu-id="1b338-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="1b338-133">**IXAudio2Voice:: setchannelvolumes**</span><span class="sxs-lookup"><span data-stu-id="1b338-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="1b338-134">**IXAudio2Voice:: Einstellungsparameter**</span><span class="sxs-lookup"><span data-stu-id="1b338-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="1b338-135">**IXAudio2Voice:: setoutputmatrix**</span><span class="sxs-lookup"><span data-stu-id="1b338-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="1b338-136">**IXAudio2Voice:: SetVolume**</span><span class="sxs-lookup"><span data-stu-id="1b338-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="1b338-137">**IXAudio2SourceVoice:: Start**</span><span class="sxs-lookup"><span data-stu-id="1b338-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="1b338-138">**IXAudio2SourceVoice:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="1b338-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="1b338-139">Wie bereits beschrieben, muss der Client Code letztendlich die Funktion [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) zum Ausführen der verzögerten Änderungen aufruft.</span><span class="sxs-lookup"><span data-stu-id="1b338-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b338-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b338-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b338-141">Vorgangs Sätze</span><span class="sxs-lookup"><span data-stu-id="1b338-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="1b338-142">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="1b338-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="1b338-143">So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz</span><span class="sxs-lookup"><span data-stu-id="1b338-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
