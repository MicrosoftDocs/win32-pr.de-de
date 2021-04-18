---
title: Player. KeyPress-Ereignis
description: Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird. | Player. KeyPress-Ereignis
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- KeyPress-Ereignisfenster Media Player
- KeyPress-Ereignisfenster Media Player, Player-Klasse
- Windows Media Player Player-Klasse, KeyPress-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371030"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="54591-107">Player. KeyPress-Ereignis</span><span class="sxs-lookup"><span data-stu-id="54591-107">Player.KeyPress event</span></span>

<span data-ttu-id="54591-108">Das **KeyPress** -Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="54591-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="54591-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="54591-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="54591-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="54591-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54591-111">*nkeyascii*</span><span class="sxs-lookup"><span data-stu-id="54591-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="54591-112">**Number** (**int**) gibt den standardmäßigen numerischen ANSI-Code für das Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="54591-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54591-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54591-113">Return value</span></span>

<span data-ttu-id="54591-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54591-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54591-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54591-115">Remarks</span></span>

<span data-ttu-id="54591-116">Dieses Ereignis tritt auf, wenn die Tastatureingabe ein beliebiges druckbares Tastatur Zeichen ergibt, die STRG-Taste mit einem Zeichen aus dem Standard Alphabet oder einem von einigen Sonderzeichen und der Eingabe-oder RÜCKTASTE gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="54591-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="54591-117">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="54591-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="54591-118">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="54591-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="54591-119">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="54591-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="54591-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54591-120">Requirements</span></span>



| <span data-ttu-id="54591-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54591-121">Requirement</span></span> | <span data-ttu-id="54591-122">Wert</span><span class="sxs-lookup"><span data-stu-id="54591-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54591-123">Version</span><span class="sxs-lookup"><span data-stu-id="54591-123">Version</span></span><br/> | <span data-ttu-id="54591-124">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="54591-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="54591-125">DLL</span><span class="sxs-lookup"><span data-stu-id="54591-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="54591-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54591-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54591-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54591-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54591-128">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="54591-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





