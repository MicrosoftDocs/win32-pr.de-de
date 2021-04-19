---
title: Player. Error-Ereignis
description: Das Fehler Ereignis tritt auf, wenn eine Fehlerbedingung vorliegt.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Fehler Ereignis-Windows-Media Player
- Fehler Ereignis Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, Fehler Ereignis
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355936"
---
# <a name="playererror-event"></a><span data-ttu-id="e0c91-106">Player. Error-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e0c91-106">Player.Error event</span></span>

<span data-ttu-id="e0c91-107">Das **Fehler** Ereignis tritt auf, wenn eine Fehlerbedingung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="e0c91-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0c91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0c91-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="e0c91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0c91-109">Parameters</span></span>

<span data-ttu-id="e0c91-110">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="e0c91-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0c91-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0c91-111">Return value</span></span>

<span data-ttu-id="e0c91-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e0c91-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="e0c91-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0c91-113">Examples</span></span>

<span data-ttu-id="e0c91-114">Im folgenden JScript-Beispiel wird ein Ereignishandler erstellt, um den Beschreibungstext für den ersten Fehler in der Fehler Warteschlange anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e0c91-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="e0c91-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0c91-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="e0c91-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0c91-116">Requirements</span></span>



| <span data-ttu-id="e0c91-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0c91-117">Requirement</span></span> | <span data-ttu-id="e0c91-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e0c91-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0c91-119">Version</span><span class="sxs-lookup"><span data-stu-id="e0c91-119">Version</span></span><br/> | <span data-ttu-id="e0c91-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e0c91-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e0c91-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e0c91-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0c91-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0c91-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0c91-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0c91-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c91-124">**ErrorItem. ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e0c91-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="e0c91-125">**Error. Item**</span><span class="sxs-lookup"><span data-stu-id="e0c91-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="e0c91-126">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e0c91-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





