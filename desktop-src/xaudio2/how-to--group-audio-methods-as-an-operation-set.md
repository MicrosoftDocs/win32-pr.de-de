---
description: In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppieren, sodass Sie gleichzeitig wirksam werden.
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: "So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866484"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="6dd3f-103">So wird's gemacht: Gruppieren von Audiomethoden als Vorgangssatz</span><span class="sxs-lookup"><span data-stu-id="6dd3f-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="6dd3f-104">In diesem Thema erfahren Sie, wie Sie XAudio2-Methoden gruppieren, sodass Sie gleichzeitig wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="6dd3f-105">So gruppieren Sie Audiomethoden als Vorgangs Satz</span><span class="sxs-lookup"><span data-stu-id="6dd3f-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="6dd3f-106">Deklarieren Sie einen globalen Vorgangs Satz-Zählers.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="6dd3f-107">Der [Vorgangs Satz](operation-sets.md) -Counter stellt sicher, dass jeder Vorgangs Satz eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="6dd3f-108">Erhöhen Sie den globalen Counter.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-108">Increment the global counter.</span></span>

    <span data-ttu-id="6dd3f-109">Jedes Mal, wenn Sie einen neuen [Vorgangs Satz](operation-sets.md)übermitteln, sollte der globale gegen Schritt erhöht werden, um sicherzustellen, dass jeder Satz eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="6dd3f-110">Gruppieren Sie die Methodenaufrufe durch Festlegen der Parameter für den [Vorgangs Satz](operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="6dd3f-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="6dd3f-111">Legen Sie die Parameter des [Vorgangs Satzes](operation-sets.md) auf den aktuellen Wert des globalen Leistungs Zählers fest.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="6dd3f-112">In diesem Fall werden vier Aufrufe von [**IXAudio2SourceVoice:: Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) als ein [Vorgangs Satz](operation-sets.md)gruppiert.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="6dd3f-113">Das Gruppieren der Aufrufe bewirkt, dass alle vier Sounds gleichzeitig gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="6dd3f-114">Starten Sie den [Vorgangs Satz](operation-sets.md).</span><span class="sxs-lookup"><span data-stu-id="6dd3f-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="6dd3f-115">Nachdem Sie alle Methoden im Satz aufgerufen haben, starten Sie den Satz durch Aufrufen von [**IXAudio2:: CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) mit dem aktuellen Wert des globalen Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="6dd3f-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6dd3f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd3f-117">Vorgangs Sätze</span><span class="sxs-lookup"><span data-stu-id="6dd3f-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="6dd3f-118">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="6dd3f-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="6dd3f-119">XAudio2-Vorgangs Sätze</span><span class="sxs-lookup"><span data-stu-id="6dd3f-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
