---
title: Zugreifen auf nicht transparente Zeiger
description: Clients können auf die in Zielen gespeicherten Informationen mithilfe von nicht transparenten Zeigern zugreifen.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515878"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="57d0b-103">Zugreifen auf nicht transparente Zeiger</span><span class="sxs-lookup"><span data-stu-id="57d0b-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="57d0b-104">Clients können auf die in Zielen gespeicherten Informationen mithilfe von nicht transparenten Zeigern zugreifen.</span><span class="sxs-lookup"><span data-stu-id="57d0b-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="57d0b-105">Um den Speicher zu verwenden, muss der Client zuerst [**rtmgetopaqueinformationpointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) aufrufen, um den Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="57d0b-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="57d0b-106">Wenn eine Änderung an den Informationen erforderlich ist, muss der Client zunächst das Ziel durch Aufrufen von [**rtmlockdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) sperren, wobei der *Lock dest* -Parameter auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57d0b-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="57d0b-107">Wenn das Ziel gesperrt ist, kann der Client die erforderlichen Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="57d0b-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="57d0b-108">Das Ziel kann mithilfe eines anderen **rtmlockdestination** -Aufrufes entsperrt werden, wobei der *Lock dest* -Parameter auf **false** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57d0b-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="57d0b-109">Die [**rtmlockdestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) -Funktion ermöglicht es einem Client auch, mithilfe des *exklusiven* Parameters entweder eine Lesesperre oder eine Schreibsperre zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="57d0b-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="57d0b-110">Ein Client sollte die Schreibsperre nur dann verwenden, wenn er Änderungen an den Informationen vornimmt, die mithilfe des nicht transparenten Zeigers gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="57d0b-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="57d0b-111">Clients können die Lesesperre verwenden, um die in einem Ziel gespeicherten nicht transparenten Zeiger Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="57d0b-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="57d0b-112">Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [zugreifen auf den nicht transparenten Zeiger in einem Ziel](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="57d0b-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




