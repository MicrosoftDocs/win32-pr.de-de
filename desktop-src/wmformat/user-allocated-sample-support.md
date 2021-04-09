---
title: Vom Benutzer zugewiesene Beispiel Unterstützung
description: Vom Benutzer zugewiesene Beispiel Unterstützung
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media-Format-SDK, vom Benutzer zugewiesene Beispiel Unterstützung
- Advanced Systems Format (ASF), vom Benutzer zugeordnete Beispiel Unterstützung
- ASF (Advanced Systems Format), vom Benutzer zugeordnete Beispiel Unterstützung
- vom Benutzer zugewiesene Beispiel Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80d6a0d9a7e19b46940093fc370bd2c8c70590d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036721"
---
# <a name="user-allocated-sample-support"></a><span data-ttu-id="b7f05-107">Vom Benutzer zugewiesene Beispiel Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b7f05-107">User Allocated Sample Support</span></span>

<span data-ttu-id="b7f05-108">Unter normalen Umständen erstellen sowohl das Reader-Objekt als auch das synchrone Reader-Objekt ein neues Buffer-Objekt für jedes Beispiel, das an die Anwendung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="b7f05-108">Under normal circumstances, both the reader object and the synchronous reader object create a new buffer object for each sample delivered to your application.</span></span> <span data-ttu-id="b7f05-109">Dies liegt daran, dass das Lese Objekt nicht weiß, wie Ihre Anwendung die Beispiele durchführt, nachdem Sie sie abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="b7f05-109">This is because the reading object has no way of knowing what your application does with the samples after it gets them.</span></span> <span data-ttu-id="b7f05-110">Obwohl viele Anwendungen nur Beispiele lesen, um Sie sofort zu Rendering, müssen einige Anwendungen möglicherweise lange Zeit Beispiele verwalten.</span><span class="sxs-lookup"><span data-stu-id="b7f05-110">Even though many applications read samples only to render them immediately, some applications may need to maintain samples for a long time.</span></span> <span data-ttu-id="b7f05-111">Das Lese Objekt kann daher keinen der von ihm zugewiesenen Puffer wieder verwenden. Sie werden an Ihre Anwendung übermittelt, die dann die Kontrolle darüber hat.</span><span class="sxs-lookup"><span data-stu-id="b7f05-111">The reading object cannot, therefore, reuse any of the buffers it allocates; it delivers them to your application, which then has control over them.</span></span>

<span data-ttu-id="b7f05-112">Das Problem bei diesem Ansatz besteht darin, dass eine Datei eine immense Anzahl von Stichproben enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="b7f05-112">The problem with this approach is that a file can contain an immense number of samples.</span></span> <span data-ttu-id="b7f05-113">Wenn für jedes von Ihnen ein neues Puffer Objekt erstellt werden muss, wird die Zuordnung und Freigabe von Arbeitsspeicher viel Prozessorzeit verschwendet.</span><span class="sxs-lookup"><span data-stu-id="b7f05-113">If each one of them requires a new buffer object to be created, a lot of processor time is wasted allocating and releasing memory.</span></span> <span data-ttu-id="b7f05-114">Bei zeitsensiblen Anwendungen, wie z. b. Media Players, kann sich dieser Aufwand stark auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="b7f05-114">In time-sensitive applications such as media players, this overhead can be very detrimental to performance.</span></span>

<span data-ttu-id="b7f05-115">Um die Leistungsprobleme der von Lesern zugewiesenen Beispiele zu verringern, unterstützen sowohl der Reader als auch der synchrone Reader vom Benutzer zugeordnete Beispiele.</span><span class="sxs-lookup"><span data-stu-id="b7f05-115">To alleviate the performance issues of reader-allocated samples, both the reader and the synchronous reader support user-allocated samples.</span></span> <span data-ttu-id="b7f05-116">Um die von der Anwendung zugeordneten Beispiele verwenden zu können, führt das Lese Objekt Aufrufe an eine von Ihnen implementierte Beispiel-Zuweisungs Rückruf Methode aus.</span><span class="sxs-lookup"><span data-stu-id="b7f05-116">To use samples allocated by your application, the reading object makes calls to a sample allocation callback method that you implement.</span></span> <span data-ttu-id="b7f05-117">Die Logik, die vom Rückruf verwendet wird, um Puffer an das Lese Objekt zu übermitteln, ist vollständig.</span><span class="sxs-lookup"><span data-stu-id="b7f05-117">The logic used by the callback to deliver buffers to the reading object is entirely up to you.</span></span> <span data-ttu-id="b7f05-118">Sie können einen Pufferpool für die gesamte Datei verwenden oder mehrere Pufferpools verwenden, einen für jede Ausgabe oder einen Stream bzw. ein beliebiges anderes Schema, das für Ihre Anwendung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="b7f05-118">You can use a pool of buffers for the entire file or use multiple pools of buffers, one for each output or stream, or any other scheme that works for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7f05-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7f05-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7f05-120">**Puffer für Datei Lesevorgänge werden zugewiesen.**</span><span class="sxs-lookup"><span data-stu-id="b7f05-120">**Allocating Buffers for File Reading**</span></span>](allocating-buffers-for-file-reading.md)
</dt> <dt>

[<span data-ttu-id="b7f05-121">**Funktionen zum Lesen von Dateien**</span><span class="sxs-lookup"><span data-stu-id="b7f05-121">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




