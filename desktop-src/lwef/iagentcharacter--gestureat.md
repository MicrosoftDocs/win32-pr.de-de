---
title: Iagentcharacter gestureat
description: Iagentcharacter gestureat
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388815"
---
# <a name="iagentcharactergestureat"></a><span data-ttu-id="497bc-103">Iagentcharacter:: gestureat</span><span class="sxs-lookup"><span data-stu-id="497bc-103">IAgentCharacter::GestureAt</span></span>

<span data-ttu-id="497bc-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="497bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="497bc-105">Gibt die zugehörige Status Animation des **gesturten** Zustands basierend auf der angegebenen Position wieder.</span><span class="sxs-lookup"><span data-stu-id="497bc-105">Plays the associated **Gesturing** state animation based on the specified location.</span></span>

-   <span data-ttu-id="497bc-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="497bc-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="497bc-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="497bc-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="497bc-108"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="497bc-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="497bc-109">Die x-Koordinate der angegebenen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="497bc-109">The x-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="497bc-110"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="497bc-110"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="497bc-111">Die y-Koordinate der angegebenen Position in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="497bc-111">The y-coordinate of the specified location in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="497bc-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="497bc-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="497bc-113">Adresse einer Variablen, die die **gestureat** -Anforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="497bc-113">Address of a variable that receives the **GestureAt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="497bc-114">Der Server ermittelt und gibt die entsprechende gesturinganimation automatisch basierend auf der aktuellen Position des Zeichens und der angegebenen Position wieder.</span><span class="sxs-lookup"><span data-stu-id="497bc-114">The server automatically determines and plays the appropriate gesturing animation based on the character's current position and the specified location.</span></span> <span data-ttu-id="497bc-115">Verwenden Sie bei Verwendung des HTTP-Protokolls für den Zugriff auf Zeichen-und Animationsdaten die [**Prepare**](iagentcharacter--prepare.md) -Methode, um sicherzustellen, dass die Animationen verfügbar sind, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="497bc-115">When using the HTTP protocol to access character and animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure that the animations are available before calling this method.</span></span>

 

 




