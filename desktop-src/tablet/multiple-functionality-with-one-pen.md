---
description: Ein Tablet PC-Stift hat möglicherweise mehr als ein Ende, das mit dem Digitalisierer interagieren kann.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Mehrere Funktionen mit einem Stift
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349879"
---
# <a name="multiple-functionality-with-one-pen"></a><span data-ttu-id="bff64-103">Mehrere Funktionen mit einem Stift</span><span class="sxs-lookup"><span data-stu-id="bff64-103">Multiple Functionality with One Pen</span></span>

<span data-ttu-id="bff64-104">Ein Tablet PC-Stift hat möglicherweise mehr als ein Ende, das mit dem Digitalisierer interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="bff64-104">A Tablet PC pen may have more than one end that can interact with the digitizer.</span></span> <span data-ttu-id="bff64-105">Wenn beide Enden des Stifts Ereignisse generieren können, kann ein Ende verwendet werden, um frei Hand Eingaben, SELECT-und Point-Funktionen zu verwenden, und das andere Ende kann für andere Funktionen wie z. b. das Löschen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bff64-105">If both ends of the pen can generate events, one end may be used to lay down ink, select, and point, and the other end may be used for other functions such as erasing.</span></span>

<span data-ttu-id="bff64-106">Um diese Funktionalität zu implementieren, muss Ihre Anwendung in der Lage sein, zu bestimmen, welches Ende des Stifts verwendet wird, und damit, wann die Darstellung des Cursors geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bff64-106">To implement such functionality, your application must be able to determine which end of the pen is being used and hence when to change the appearance of the cursor.</span></span> <span data-ttu-id="bff64-107">Dies ist möglich, indem Sie den Status der [**invertierten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) Eigenschaft für das [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt suchen.</span><span class="sxs-lookup"><span data-stu-id="bff64-107">It can do this by looking for the state of the [**Inverted**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) property on the [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

<span data-ttu-id="bff64-108">Ausführliche Informationen zur Verwendung der Rückseite des Stifts zum Löschen finden Sie unter Löschen von frei Hand Eingaben [mit dem Stift](erasing-ink-with-the-pen.md).</span><span class="sxs-lookup"><span data-stu-id="bff64-108">For specific details about using the back of the pen for erasing, see [Erasing Ink with the Pen](erasing-ink-with-the-pen.md).</span></span> <span data-ttu-id="bff64-109">Außerdem wird im [Beispiel](ink-erasing-sample.md) frei Hand Löschung veranschaulicht, wie die Rückseite des Stifts verwendet wird, um frei Hand Eingaben zu löschen.</span><span class="sxs-lookup"><span data-stu-id="bff64-109">In addition, the [Ink Erasing Sample](ink-erasing-sample.md) demonstrates how to use the back of the pen to erase ink.</span></span>

 

 



