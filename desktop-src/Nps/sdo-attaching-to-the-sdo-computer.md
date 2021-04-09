---
title: Anfügen an den SDO-Computer
description: Mit dem Schnittstellen Zeiger, der von cokreateinstance zurückgegeben wurde, wird die isdomachine Attach-Methode aufgerufen.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948816"
---
# <a name="attaching-to-the-sdo-computer"></a><span data-ttu-id="8b70f-103">Anfügen an den SDO-Computer</span><span class="sxs-lookup"><span data-stu-id="8b70f-103">Attaching to the SDO Computer</span></span>

<span data-ttu-id="8b70f-104">Mit dem Schnittstellen Zeiger, der von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)zurückgegeben wurde, können Sie die [**isdomachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b70f-104">With the interface pointer returned by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), call the [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) method.</span></span> <span data-ttu-id="8b70f-105">Übergeben Sie **null** als Parameter an die **Attach** -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b70f-105">Pass **NULL** as the parameter to the **Attach** method.</span></span> <span data-ttu-id="8b70f-106">Der Wert **null** gibt an, dass **Attach** das Computer Objekt dem lokalen Computer zuordnen soll.</span><span class="sxs-lookup"><span data-stu-id="8b70f-106">The value **NULL** specifies that **Attach** associate the machine object with the local computer.</span></span> <span data-ttu-id="8b70f-107">Das Anfügen an einen Remote Computer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b70f-107">Attaching to a remote computer is not supported.</span></span>

<span data-ttu-id="8b70f-108">Um festzustellen, ob der lokale Computer bereits angefügt ist, müssen Sie die [**isdomachine:: getattachedcomputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b70f-108">To determine if the local computer is already attached, call the [**ISdoMachine::GetAttachedComputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) method.</span></span>

<span data-ttu-id="8b70f-109">Beispielcode, der das Anfügen an den lokalen Computer veranschaulicht, finden [Sie unter Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .</span><span class="sxs-lookup"><span data-stu-id="8b70f-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to attach to the local computer.</span></span>

 

 