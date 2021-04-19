---
title: Network. bufferingcount
description: Die bufferingcount-Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Clip Wiedergabe erfolgt ist.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Network. bufferingcount-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370012"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="d7fb0-104">Network. bufferingcount</span><span class="sxs-lookup"><span data-stu-id="d7fb0-104">Network.bufferingCount</span></span>

<span data-ttu-id="d7fb0-105">Die **bufferingcount** -Eigenschaft ruft die Häufigkeit ab, mit der die Pufferung während der Clip Wiedergabe erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fb0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7fb0-106">Syntax</span></span>

<span data-ttu-id="d7fb0-107">*Player*. *Netzwerk*. **bufferingcount**</span><span class="sxs-lookup"><span data-stu-id="d7fb0-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d7fb0-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d7fb0-108">Possible Values</span></span>

<span data-ttu-id="d7fb0-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="d7fb0-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7fb0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7fb0-110">Remarks</span></span>

<span data-ttu-id="d7fb0-111">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="d7fb0-112">Wenn die Wiedergabe angehalten wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="d7fb0-113">Die Pufferung gilt nur für Streaminginhalte.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="d7fb0-114">Diese Eigenschaft gibt gültige Informationen nur zur Laufzeit zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="d7fb0-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7fb0-115">Examples</span></span>

<span data-ttu-id="d7fb0-116">Im folgenden JScript-Beispiel wird *Network* verwendet. **bufferingcount** , um anzuzeigen, wie oft die Pufferung während der Wiedergabe auftritt.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="d7fb0-117">Die Informationen werden in einem HTML div-Code angezeigt, der mit ID = "CB" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="d7fb0-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="d7fb0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7fb0-119">Requirements</span></span>



| <span data-ttu-id="d7fb0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7fb0-120">Requirement</span></span> | <span data-ttu-id="d7fb0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d7fb0-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fb0-122">Version</span><span class="sxs-lookup"><span data-stu-id="d7fb0-122">Version</span></span><br/> | <span data-ttu-id="d7fb0-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d7fb0-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d7fb0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d7fb0-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7fb0-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7fb0-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fb0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7fb0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fb0-127">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="d7fb0-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="d7fb0-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="d7fb0-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





