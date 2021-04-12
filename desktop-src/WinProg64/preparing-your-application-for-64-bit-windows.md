---
title: Vorbereiten der Anwendung für 64-Bit-Windows
description: Es gibt mehrere Features, die es Ihnen erleichtern, Anwendungen zu entwickeln, die auf 32-und 64-Bit-Fenstern ausgeführt werden können. Die meisten dieser Informationen, wie z. b. die neuen Datentypen, werden unter Vorbereiten für 64-Bit-Windows beschrieben.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-Bit-Toolkit 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209333"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="43a2f-105">Vorbereiten der Anwendung für 64-Bit-Windows</span><span class="sxs-lookup"><span data-stu-id="43a2f-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="43a2f-106">Es gibt mehrere Features, die es Ihnen erleichtern, Anwendungen zu entwickeln, die auf 32-und 64-Bit-Fenstern ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="43a2f-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="43a2f-107">Die meisten dieser Informationen, wie z. b. die neuen Datentypen, werden unter [vorbereiten für 64-Bit-Windows](getting-ready-for-64-bit-windows.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="43a2f-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="43a2f-108">Das 64-Bit-Toolkit, das im Lieferumfang des Windows SDK enthalten ist, enthält einen 64-Bit-Mittelwert Compiler, Midl.exe, zum Erstellen von nativen 64-Bit-stubwerten sowie 32-Bit-stubwerte.</span><span class="sxs-lookup"><span data-stu-id="43a2f-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="43a2f-109">Verwenden Sie den Schalter **/env Win64** , um nur 64-Bit-stubwerte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="43a2f-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="43a2f-110">Standardmäßig werden duale stubwerte generiert, die auf beiden Plattformen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="43a2f-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="43a2f-111">Beachten Sie, dass die 64-Bit-Mittell nur die Optimierungs Modi [**/Oicf**](/windows/desktop/Midl/-oi) und [**/OS**](/windows/desktop/Midl/-os) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43a2f-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 