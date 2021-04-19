---
title: Speichern und Wiederherstellen von Sätzen von Zustandsvariablen
description: Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attribut Stapel mit den Funktionen glpushatpub und glpopatpub speichern und wiederherstellen.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- OpenGL-Zustandsvariablen
- Speichern von Zustandsvariablen OpenGL
- Wiederherstellen von Zustandsvariablen OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338601"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a><span data-ttu-id="43823-106">Speichern und Wiederherstellen von Sätzen von Zustandsvariablen</span><span class="sxs-lookup"><span data-stu-id="43823-106">Saving and Restoring Sets of State Variables</span></span>

<span data-ttu-id="43823-107">Sie können die Werte einer Auflistung von Zustandsvariablen in einem Attribut Stapel mit den Funktionen [**glpushatpub**](glpushattrib.md) und [**glpopatpub**](glpopattrib.md) speichern und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="43823-107">You can save and restore the values of a collection of state variables on an attribute stack with the [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) functions.</span></span> <span data-ttu-id="43823-108">Der Attribut Stapel hat eine Tiefe von mindestens 16.</span><span class="sxs-lookup"><span data-stu-id="43823-108">The attribute stack has a depth of at least 16.</span></span> <span data-ttu-id="43823-109">Um die tatsächliche Tiefe zu erhalten, verwenden Sie die maximale Speichergröße \_ \_ von GL \_ \_ . [](glgetintegerv.md)</span><span class="sxs-lookup"><span data-stu-id="43823-109">To obtain the actual depth, use GL\_MAX\_ATTRIB\_STACK\_DEPTH with [**glGetIntegerv**](glgetintegerv.md).</span></span> <span data-ttu-id="43823-110">Durch das übertragen eines vollständigen Stapels oder das Pop einer leeren wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="43823-110">Pushing a full stack or popping an empty one generates an error.</span></span>

<span data-ttu-id="43823-111">Es ist in der Regel schneller, **glpushatpub** und **glpopatpub** zu verwenden, als die Werte selbst zu erhalten und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="43823-111">It is generally faster to use **glPushAttrib** and **glPopAttrib** than to get and restore the values yourself.</span></span> <span data-ttu-id="43823-112">Einige Werte werden möglicherweise per pushübertragung in die Hardware übermittelt, und das Speichern und wiederherstellen kann ressourcenintensiv sein.</span><span class="sxs-lookup"><span data-stu-id="43823-112">Some values might be pushed and popped in the hardware, and saving and restoring them can be resource-intensive.</span></span> <span data-ttu-id="43823-113">Wenn Sie einen Remote Client verwenden, müssen alle Attributdaten bei der Speicherung und Wiederherstellung über die Netzwerkverbindung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="43823-113">Also, if you're operating on a remote client, all of the attribute data must be transferred across the network connection and back as it is saved and restored.</span></span> <span data-ttu-id="43823-114">Allerdings behält ihre OpenGL-Implementierung den Attribut Stapel auf dem Server bei, wodurch unnötige Netzwerkverzögerungen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="43823-114">However, your OpenGL implementation keeps the attribute stack on the server, avoiding unnecessary network delays.</span></span>

<span data-ttu-id="43823-115">Der Prototyp von **glpushatpub** ist:</span><span class="sxs-lookup"><span data-stu-id="43823-115">The prototype of **glPushAttrib** is:</span></span>

<span data-ttu-id="43823-116">**void** **glpushattestb**(**GLbitfield** *Mask* );</span><span class="sxs-lookup"><span data-stu-id="43823-116">**void** **glPushAttrib**(**GLbitfield** *mask* );</span></span>

<span data-ttu-id="43823-117">Durch die Verwendung von [**glpushatpub**](glpushattrib.md) werden alle durch Bits in der *Maske* gekennzeichneten Attribute gespeichert, indem Sie auf den Attribut Stapel übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="43823-117">Using [**glPushAttrib**](glpushattrib.md) saves all the attributes indicated by bits in *mask* by pushing them onto the attribute stack.</span></span> <span data-ttu-id="43823-118">Eine Liste der möglichen Masken Bits, die Sie logisch oder gemeinsam zum Speichern einer beliebigen Kombination von Attributen haben, finden Sie unter [Attribut Gruppen](attribute-groups.md).</span><span class="sxs-lookup"><span data-stu-id="43823-118">For a list of the possible mask bits you can logically OR together to save any combination of attributes, see [Attribute Groups](attribute-groups.md).</span></span> <span data-ttu-id="43823-119">Jedes Bit entspricht einer Auflistung einzelner Zustandsvariablen.</span><span class="sxs-lookup"><span data-stu-id="43823-119">Each bit corresponds to a collection of individual state variables.</span></span> <span data-ttu-id="43823-120">Das GL-Beleuchtungs Bit bezieht sich z. b. \_ \_ auf alle Zustandsvariablen im Zusammenhang mit der Beleuchtung, einschließlich der aktuellen Material Farbe, der Ambient-, diffuse, Glanz und ausgegebene Beleuchtung, einer Liste der aktivierten Lichter und der Richtungen der Schein Lichter.</span><span class="sxs-lookup"><span data-stu-id="43823-120">For example, GL\_LIGHTING\_BIT refers to all the state variables related to lighting, which include the current material color; the ambient, diffuse, specular, and emitted light; a list of the lights that are enabled; and the directions of the spotlights.</span></span> <span data-ttu-id="43823-121">Wenn Sie [**glpopatzb**](glpopattrib.md)anrufen, werden alle diese Variablen wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="43823-121">When you call [**glPopAttrib**](glpopattrib.md), all those variables are restored.</span></span> <span data-ttu-id="43823-122">Informationen dazu, welche Attribute für bestimmte Masken Werte gespeichert werden, finden Sie unter [OpenGL State variables](opengl-state-variables.md).</span><span class="sxs-lookup"><span data-stu-id="43823-122">To find out exactly which attributes are saved for particular mask values, see [OpenGL State Variables](opengl-state-variables.md).</span></span>

 

 




