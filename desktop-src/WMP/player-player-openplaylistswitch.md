---
title: Player. openplaylistswitch-Ereignis
description: Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt. | Player. openplaylistswitch-Ereignis
ms.assetid: 97d69716-602f-4522-b743-83f2dbc852a2
keywords:
- Media Player für openplaylistswitch-Ereignisfenster
- Openplaylistswitch-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, openplaylistswitch-Ereignis
topic_type:
- apiref
api_name:
- Player.OpenPlaylistSwitch
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d35d4568356365cc9276c13ea33f866e937da1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364642"
---
# <a name="playeropenplaylistswitch-event"></a><span data-ttu-id="009a6-107">Player. openplaylistswitch-Ereignis</span><span class="sxs-lookup"><span data-stu-id="009a6-107">Player.OpenPlaylistSwitch event</span></span>

<span data-ttu-id="009a6-108">Das **openplaylistswitch** -Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.</span><span class="sxs-lookup"><span data-stu-id="009a6-108">The **OpenPlaylistSwitch** event occurs when a title on a DVD begins playing.</span></span>

## <a name="syntax"></a><span data-ttu-id="009a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="009a6-109">Syntax</span></span>


```JScript
Player.OpenPlaylistSwitch(
  pItem
)
```



## <a name="parameters"></a><span data-ttu-id="009a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="009a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009a6-111">*pitem*</span><span class="sxs-lookup"><span data-stu-id="009a6-111">*pItem*</span></span> 
</dt> <dd>

<span data-ttu-id="009a6-112">**Wiedergabe** Listen Objekt, das den Titel darstellt.</span><span class="sxs-lookup"><span data-stu-id="009a6-112">**Playlist** object representing the title.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009a6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="009a6-113">Return value</span></span>

<span data-ttu-id="009a6-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="009a6-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="009a6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="009a6-115">Remarks</span></span>

<span data-ttu-id="009a6-116">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="009a6-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="009a6-117">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="009a6-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="009a6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="009a6-118">Requirements</span></span>



| <span data-ttu-id="009a6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="009a6-119">Requirement</span></span> | <span data-ttu-id="009a6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="009a6-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="009a6-121">Version</span><span class="sxs-lookup"><span data-stu-id="009a6-121">Version</span></span><br/> | <span data-ttu-id="009a6-122">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="009a6-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="009a6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="009a6-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="009a6-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="009a6-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="009a6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="009a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009a6-126">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="009a6-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





