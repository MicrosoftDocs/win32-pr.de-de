---
title: Network. lostpakete
description: Die lostpaketen-Eigenschaft ruft die Anzahl der verlorenen Pakete ab.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network. lostpackt-Fenster Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364720"
---
# <a name="networklostpackets"></a><span data-ttu-id="c5b86-104">Network. lostpakete</span><span class="sxs-lookup"><span data-stu-id="c5b86-104">Network.lostPackets</span></span>

<span data-ttu-id="c5b86-105">Die **lostpaketen** -Eigenschaft ruft die Anzahl der verlorenen Pakete ab.</span><span class="sxs-lookup"><span data-stu-id="c5b86-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b86-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5b86-106">Syntax</span></span>

<span data-ttu-id="c5b86-107">*Player*. *Netzwerk*. **lostpakete**</span><span class="sxs-lookup"><span data-stu-id="c5b86-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c5b86-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c5b86-108">Possible Values</span></span>

<span data-ttu-id="c5b86-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="c5b86-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5b86-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5b86-110">Remarks</span></span>

<span data-ttu-id="c5b86-111">Diese Eigenschaft ist nur für Streamingmedien gültig und gleich 0 (null), wenn das HTTP-Protokoll verwendet wird, das verlustfrei ist.</span><span class="sxs-lookup"><span data-stu-id="c5b86-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="c5b86-112">Pakete können aus verschiedenen Gründen verloren gehen, z. b. Art und Qualität der Netzwerkverbindung.</span><span class="sxs-lookup"><span data-stu-id="c5b86-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="c5b86-113">Jedes Mal, wenn die Wiedergabe beendet und neu gestartet wird, wird diese Eigenschaft auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5b86-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="c5b86-114">Wenn die Wiedergabe angehalten und neu gestartet wird, wird Sie nicht zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="c5b86-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="c5b86-115">Diese Eigenschaft gibt nur zur Laufzeit gültige Informationen und nur dann zurück, wenn der *Player*. Die **URL** -Eigenschaft ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5b86-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="c5b86-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5b86-116">Examples</span></span>

<span data-ttu-id="c5b86-117">Im folgenden JScript-Beispiel wird *Network* verwendet. **lostpakete** zum Anzeigen der Gesamtanzahl der Pakete, die während der Wiedergabe verloren gehen, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="c5b86-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="c5b86-118">Die Informationen werden in einem HTML div-Format angezeigt, das mit ID = "LP" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5b86-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="c5b86-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c5b86-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="c5b86-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5b86-120">Requirements</span></span>



| <span data-ttu-id="c5b86-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5b86-121">Requirement</span></span> | <span data-ttu-id="c5b86-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c5b86-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b86-123">Version</span><span class="sxs-lookup"><span data-stu-id="c5b86-123">Version</span></span><br/> | <span data-ttu-id="c5b86-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c5b86-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c5b86-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b86-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c5b86-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b86-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b86-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5b86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b86-128">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="c5b86-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c5b86-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="c5b86-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





