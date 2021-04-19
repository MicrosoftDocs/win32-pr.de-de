---
title: Netzwerkbandbreite
description: Die Bandbreiten Eigenschaft ruft die aktuelle Bandbreite des Clips ab.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Netzwerk-Bandbreiten Fenster Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356382"
---
# <a name="networkbandwidth"></a><span data-ttu-id="a39a4-104">Netzwerkbandbreite</span><span class="sxs-lookup"><span data-stu-id="a39a4-104">Network.bandWidth</span></span>

<span data-ttu-id="a39a4-105">Die **Bandbreiten** Eigenschaft ruft die aktuelle Bandbreite des Clips ab.</span><span class="sxs-lookup"><span data-stu-id="a39a4-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="a39a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a39a4-106">Syntax</span></span>

<span data-ttu-id="a39a4-107">*Player*. *Netzwerk*. **Bandbreite**</span><span class="sxs-lookup"><span data-stu-id="a39a4-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a39a4-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a39a4-108">Possible Values</span></span>

<span data-ttu-id="a39a4-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a39a4-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a39a4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a39a4-110">Remarks</span></span>

<span data-ttu-id="a39a4-111">Diese Eigenschaft gibt NULL zurück, wenn der *Player*. Die **URL** -Eigenschaft ist nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a39a4-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="a39a4-112">Diese Eigenschaft ist nur für Streamingmedien gültig.</span><span class="sxs-lookup"><span data-stu-id="a39a4-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="a39a4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a39a4-113">Examples</span></span>

<span data-ttu-id="a39a4-114">Im folgenden Microsoft JScript-Beispiel wird *Network* verwendet. **Bandbreite** zum Anzeigen der aktuellen Medien Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="a39a4-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="a39a4-115">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "BW" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a39a4-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="a39a4-116">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a39a4-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="a39a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a39a4-117">Requirements</span></span>



| <span data-ttu-id="a39a4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a39a4-118">Requirement</span></span> | <span data-ttu-id="a39a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a39a4-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a39a4-120">Version</span><span class="sxs-lookup"><span data-stu-id="a39a4-120">Version</span></span><br/> | <span data-ttu-id="a39a4-121">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a39a4-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a39a4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a39a4-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="a39a4-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a39a4-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a39a4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a39a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39a4-125">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="a39a4-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a39a4-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="a39a4-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





