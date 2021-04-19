---
title: Player. windowlessvideo
description: Mit der windowlessvideo-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessvideo-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359324"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="f145e-104">Player. windowlessvideo</span><span class="sxs-lookup"><span data-stu-id="f145e-104">Player.windowlessVideo</span></span>

<span data-ttu-id="f145e-105">Mit der **windowlessvideo** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.</span><span class="sxs-lookup"><span data-stu-id="f145e-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="f145e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f145e-106">Syntax</span></span>

<span data-ttu-id="f145e-107">*Player*. **windowlessvideo**</span><span class="sxs-lookup"><span data-stu-id="f145e-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f145e-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f145e-108">Possible Values</span></span>

<span data-ttu-id="f145e-109">Diese Eigenschaft ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird und danach schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="f145e-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="f145e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="f145e-110">Value</span></span> | <span data-ttu-id="f145e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f145e-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="f145e-112">true</span><span class="sxs-lookup"><span data-stu-id="f145e-112">true</span></span>  | <span data-ttu-id="f145e-113">Das Video wird im fensterlosen Modus gerendert.</span><span class="sxs-lookup"><span data-stu-id="f145e-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="f145e-114">false</span><span class="sxs-lookup"><span data-stu-id="f145e-114">false</span></span> | <span data-ttu-id="f145e-115">Standard.</span><span class="sxs-lookup"><span data-stu-id="f145e-115">Default.</span></span> <span data-ttu-id="f145e-116">Das Video wird im Fenstermodus gerendert.</span><span class="sxs-lookup"><span data-stu-id="f145e-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f145e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f145e-117">Remarks</span></span>

<span data-ttu-id="f145e-118">Standardmäßig rendert ein eingebettetes Windows-Media Player-Steuerelement Videos in einem eigenen Fenster innerhalb des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="f145e-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="f145e-119">Wenn **windowlessvideo** auf "true" festgelegt ist, rendert das Player-Steuerelement Videos direkt im Client Bereich, sodass Sie besondere Effekte anwenden oder das Video mit Text übertragen können.</span><span class="sxs-lookup"><span data-stu-id="f145e-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="f145e-120">In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="f145e-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="f145e-121">Die **windowlessvideo** -Eigenschaft wird für den Netscape-Navigator nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f145e-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="f145e-122">Wenn Sie einen Wert für diese Eigenschaft im Navigator festlegen, kann dies zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f145e-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="f145e-123">**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f145e-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f145e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f145e-124">Requirements</span></span>



| <span data-ttu-id="f145e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f145e-125">Requirement</span></span> | <span data-ttu-id="f145e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f145e-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f145e-127">Version</span><span class="sxs-lookup"><span data-stu-id="f145e-127">Version</span></span><br/> | <span data-ttu-id="f145e-128">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="f145e-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="f145e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f145e-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="f145e-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f145e-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





