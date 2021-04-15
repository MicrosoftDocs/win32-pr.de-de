---
title: Dynamische pufferserialisierung
description: Bei Verwendung der dynamischen Pufferart der Serialisierung wird der marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie zurückgegeben. Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der die Daten enthält.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471260"
---
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="1f00d-104">Dynamische pufferserialisierung</span><span class="sxs-lookup"><span data-stu-id="1f00d-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="1f00d-105">Bei Verwendung der dynamischen Pufferart der Serialisierung wird der marshallingpuffer vom Stub zugeordnet, und die Daten werden in diesen Puffer codiert und an Sie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1f00d-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="1f00d-106">Wenn Sie das Marshalling durchlaufen, stellen Sie den Puffer bereit, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="1f00d-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="1f00d-107">Der dynamische pufferstil der Serialisierung verwendet die folgenden Routinen:</span><span class="sxs-lookup"><span data-stu-id="1f00d-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="1f00d-108">**Mesencoentdynbufferlenker Create**</span><span class="sxs-lookup"><span data-stu-id="1f00d-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="1f00d-109">**Mesdecodebufferlagercreate**</span><span class="sxs-lookup"><span data-stu-id="1f00d-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="1f00d-110">**Mesbufferhandlereset**</span><span class="sxs-lookup"><span data-stu-id="1f00d-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="1f00d-111">**Meslenker frei**</span><span class="sxs-lookup"><span data-stu-id="1f00d-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="1f00d-112">Die [**mesencodebug**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) -Funktion ordnet den für das Codierungs handle benötigten Arbeitsspeicher zu und initialisiert Sie dann.</span><span class="sxs-lookup"><span data-stu-id="1f00d-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="1f00d-113">Die Anwendung kann [**mesbufferhandlereset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) aufrufen, um das Handle erneut zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1f00d-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="1f00d-114">Sie ruft [**meslenker frei**](/windows/desktop/api/Midles/nf-midles-meshandlefree) auf, um den Arbeitsspeicher des Handles freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1f00d-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="1f00d-115">Zum Erstellen eines Decodierungs Handles, das dem dynamischen Puffer Codierungs Handle entspricht, verwenden Sie [**mesdecodebufferlenker Create**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="1f00d-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




