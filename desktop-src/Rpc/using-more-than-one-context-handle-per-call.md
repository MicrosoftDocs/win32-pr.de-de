---
title: Verwenden von mehr als einem Kontext Handle pro Rückruf
description: Die Möglichkeit, Arrays von Kontext Handles als Parameter zu verwenden, wird in Windows Vista und höheren Betriebssystemen zur Verfügung gestellt.
ms.assetid: 84f3036b-ff4d-485d-bf23-ad10a03076a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7b1c69dd182bee8f68e7068bcfcef60efd380a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856135"
---
# <a name="using-more-than-one-context-handle-per-call"></a><span data-ttu-id="0aa31-103">Verwenden von mehr als einem Kontext Handle pro Rückruf</span><span class="sxs-lookup"><span data-stu-id="0aa31-103">Using More than One Context Handle per Call</span></span>

<span data-ttu-id="0aa31-104">Die Möglichkeit, Arrays von Kontext Handles als Parameter zu verwenden, wird in Windows Vista und höheren Betriebssystemen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="0aa31-104">The ability to use arrays of context handles as parameters is made available in Windows Vista and later operating systems.</span></span> <span data-ttu-id="0aa31-105">Diese Funktion sollte jedoch in einer Anwendung sorgfältig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0aa31-105">However, this feature should be used carefully within an application.</span></span> <span data-ttu-id="0aa31-106">In einer Situation, in der ein Kontext Handle in mehreren Aufrufen verwendet wird, wird es zunehmend schwieriger, seine Verwendung nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="0aa31-106">For example, in a situation where a context handle is being used in multiple calls it becomes increasingly difficult to keep track of its use.</span></span>

 

 




