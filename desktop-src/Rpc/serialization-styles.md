---
title: Serialisierungsstile
description: Es gibt drei Stile, die Sie verwenden können, um serialisierungshandles zu bearbeiten.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388516"
---
# <a name="serialization-styles"></a><span data-ttu-id="bfdde-103">Serialisierungsstile</span><span class="sxs-lookup"><span data-stu-id="bfdde-103">Serialization Styles</span></span>

<span data-ttu-id="bfdde-104">Es gibt drei Stile, die Sie verwenden können, um serialisierungshandles zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bfdde-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="bfdde-105">Diese lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bfdde-105">These are:</span></span>

-   [<span data-ttu-id="bfdde-106">Serialisierung fester Puffer</span><span class="sxs-lookup"><span data-stu-id="bfdde-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="bfdde-107">Dynamische pufferserialisierung</span><span class="sxs-lookup"><span data-stu-id="bfdde-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="bfdde-108">Krementelle Serialisierung</span><span class="sxs-lookup"><span data-stu-id="bfdde-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="bfdde-109">Unabhängig vom verwendeten Stil müssen Sie ein serialisierungshandle erstellen, die Daten serialisieren und dann das Handle freigeben.</span><span class="sxs-lookup"><span data-stu-id="bfdde-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="bfdde-110">Der Stil wird festgelegt, wenn das Programm das Handle erstellt und die Art und Weise definiert, wie ein Puffer manipuliert wird.</span><span class="sxs-lookup"><span data-stu-id="bfdde-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="bfdde-111">Das Handle behält den entsprechenden Kontext bei, der jedem der drei serialisierungsstile zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bfdde-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




