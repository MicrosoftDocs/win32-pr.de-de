---
title: Player. mediachange-Ereignis
description: Das mediachange-Ereignis tritt auf, wenn ein Medien Element geändert wird. | Player. mediachange-Ereignis
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Media Player "mediachange-Ereignisfenster"
- Mediachange-Ereignisfenster Media Player, Player-Klasse
- Player-Klasse Windows Media Player, mediachange-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372690"
---
# <a name="playermediachange-event"></a><span data-ttu-id="abc30-107">Player. mediachange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="abc30-107">Player.MediaChange event</span></span>

<span data-ttu-id="abc30-108">Das **mediachange** -Ereignis tritt auf, wenn ein Medien Element geändert wird.</span><span class="sxs-lookup"><span data-stu-id="abc30-108">The **MediaChange** event occurs when a media item changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc30-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="abc30-109">Syntax</span></span>


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a><span data-ttu-id="abc30-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="abc30-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abc30-111">*Element*</span><span class="sxs-lookup"><span data-stu-id="abc30-111">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="abc30-112">**Medien** Objekt, das das geänderte Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="abc30-112">**Media** object representing the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abc30-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abc30-113">Return value</span></span>

<span data-ttu-id="abc30-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="abc30-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="abc30-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abc30-115">Remarks</span></span>

<span data-ttu-id="abc30-116">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="abc30-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="abc30-117">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="abc30-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="abc30-118">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abc30-118">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="abc30-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abc30-119">Examples</span></span>

<span data-ttu-id="abc30-120">Im folgenden JScript-Beispiel wird ein HTML-div-Element mit dem Namen "MEDIANAME" verwendet, um den Namen des aktuellen Medien Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="abc30-120">The following JScript example uses an HTML DIV element, named MediaName, to display the name of the current media item.</span></span> <span data-ttu-id="abc30-121">Der Code aktualisiert den Text im div-Element mit jedem Vorkommen des **mediachange** -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="abc30-121">The code updates the text in the DIV with each occurrence of the **mediaChange** event.</span></span> <span data-ttu-id="abc30-122">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="abc30-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="abc30-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abc30-123">Requirements</span></span>



| <span data-ttu-id="abc30-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abc30-124">Requirement</span></span> | <span data-ttu-id="abc30-125">Wert</span><span class="sxs-lookup"><span data-stu-id="abc30-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abc30-126">Version</span><span class="sxs-lookup"><span data-stu-id="abc30-126">Version</span></span><br/> | <span data-ttu-id="abc30-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="abc30-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="abc30-128">DLL</span><span class="sxs-lookup"><span data-stu-id="abc30-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="abc30-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abc30-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abc30-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abc30-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abc30-131">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="abc30-131">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





