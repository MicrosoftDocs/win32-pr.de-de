---
title: Iagentcharacter-muveto
description: Iagentcharacter-muveto
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038865"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="02ed5-103">Iagentcharacter:: muveto</span><span class="sxs-lookup"><span data-stu-id="02ed5-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="02ed5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="02ed5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="02ed5-105">Gibt die zugehörige **Bewegungs** Zustands Animation wieder und verschiebt den Zeichen Rahmen an die angegebene Position.</span><span class="sxs-lookup"><span data-stu-id="02ed5-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="02ed5-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="02ed5-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="02ed5-107">Wenn die Funktion zurückgibt, enthält diese Variable die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="02ed5-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="02ed5-108"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="02ed5-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="02ed5-109">Die x-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="02ed5-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="02ed5-110">Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.</span><span class="sxs-lookup"><span data-stu-id="02ed5-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="02ed5-111"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="02ed5-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="02ed5-112">Die y-Koordinate der neuen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="02ed5-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="02ed5-113">Der Speicherort eines Zeichens basiert auf der linken oberen Ecke des Animations Rahmens.</span><span class="sxs-lookup"><span data-stu-id="02ed5-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="02ed5-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lspeed*</span><span class="sxs-lookup"><span data-stu-id="02ed5-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="02ed5-115">Ein Parameter, der in Millisekunden angibt, wie schnell der Rahmen des Zeichens bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="02ed5-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="02ed5-116">Der empfohlene Wert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="02ed5-116">The recommended value is 1000.</span></span> <span data-ttu-id="02ed5-117">Durch die Angabe von NULL (0) wird der Frame verschoben, ohne eine Animation zu spielen.</span><span class="sxs-lookup"><span data-stu-id="02ed5-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="02ed5-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="02ed5-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="02ed5-119">Adresse einer Variablen, [**die die Anforderung**](https://www.bing.com/search?q=**MoveTo**) -ID für das anforderungspaar empfängt.</span><span class="sxs-lookup"><span data-stu-id="02ed5-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="02ed5-120">Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichen-und Animationsdaten verwenden, verwenden Sie die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um die Verfügbarkeit der **Bewegungs** Zustands Animationen vor dem Aufrufen dieser Methode sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="02ed5-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="02ed5-121">Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame noch immer.</span><span class="sxs-lookup"><span data-stu-id="02ed5-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="02ed5-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="02ed5-122">See Also</span></span>

[<span data-ttu-id="02ed5-123">**Iagentcharacter:: SetPosition**</span><span class="sxs-lookup"><span data-stu-id="02ed5-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 