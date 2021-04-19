---
title: Player. audiolanguagechange-Ereignis
description: Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | Player. audiolanguagechange-Ereignis
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player für audiolanguagechange-Ereignisfenster
- Audiolanguagechange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, audiolanguagechange-Ereignis
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373724"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="604ed-107">Player. audiolanguagechange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="604ed-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="604ed-108">Das **audiolanguagechange** -Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert.</span><span class="sxs-lookup"><span data-stu-id="604ed-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="604ed-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="604ed-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="604ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="604ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604ed-111">*LangID*</span><span class="sxs-lookup"><span data-stu-id="604ed-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="604ed-112">**Number** (**Long**), der den neuen Gebiets Schema Bezeichner (LCID) angibt.</span><span class="sxs-lookup"><span data-stu-id="604ed-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604ed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="604ed-113">Return value</span></span>

<span data-ttu-id="604ed-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="604ed-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="604ed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="604ed-115">Remarks</span></span>

<span data-ttu-id="604ed-116">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="604ed-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="604ed-117">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten Microsoft JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="604ed-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="604ed-118">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="604ed-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="604ed-119">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="604ed-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="604ed-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="604ed-120">Requirements</span></span>



| <span data-ttu-id="604ed-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="604ed-121">Requirement</span></span> | <span data-ttu-id="604ed-122">Wert</span><span class="sxs-lookup"><span data-stu-id="604ed-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="604ed-123">Version</span><span class="sxs-lookup"><span data-stu-id="604ed-123">Version</span></span><br/> | <span data-ttu-id="604ed-124">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="604ed-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="604ed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="604ed-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="604ed-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="604ed-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604ed-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="604ed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="604ed-128">**Controls. currentaudiolanguage**</span><span class="sxs-lookup"><span data-stu-id="604ed-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="604ed-129">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="604ed-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





