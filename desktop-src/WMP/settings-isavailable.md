---
title: Settings. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | Settings. IsAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- "\"Settings. IsAvailable\"-Windows-Media Player"
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370660"
---
# <a name="settingsisavailable"></a><span data-ttu-id="7f762-105">Settings. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="7f762-105">Settings.isAvailable</span></span>

<span data-ttu-id="7f762-106">Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f762-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f762-107">Syntax</span></span>

<span data-ttu-id="7f762-108">Player. Settings. IsAvailable (Name)</span><span class="sxs-lookup"><span data-stu-id="7f762-108">player.settings.isAvailable( name )</span></span>

## <a name="parameters"></a><span data-ttu-id="7f762-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f762-109">Parameters</span></span>

<span data-ttu-id="7f762-110">*name*</span><span class="sxs-lookup"><span data-stu-id="7f762-110">*name*</span></span>

<span data-ttu-id="7f762-111">Eine Zeichenfolge, die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="7f762-111">String containing one of the following values.</span></span>



| <span data-ttu-id="7f762-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7f762-112">String</span></span>             | <span data-ttu-id="7f762-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f762-113">Description</span></span>                                                    |
|--------------------|----------------------------------------------------------------|
| <span data-ttu-id="7f762-114">AutoStart</span><span class="sxs-lookup"><span data-stu-id="7f762-114">AutoStart</span></span>          | <span data-ttu-id="7f762-115">Bestimmt, ob die Autostart-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-115">Determines whether the autoStart property can be set.</span></span>          |
| <span data-ttu-id="7f762-116">Balance</span><span class="sxs-lookup"><span data-stu-id="7f762-116">Balance</span></span>            | <span data-ttu-id="7f762-117">Bestimmt, ob die Balance-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-117">Determines whether the balance property can be set.</span></span>            |
| <span data-ttu-id="7f762-118">Basis</span><span class="sxs-lookup"><span data-stu-id="7f762-118">BaseURL</span></span>            | <span data-ttu-id="7f762-119">Bestimmt, ob die baseurl-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-119">Determines whether the baseURL property can be set.</span></span>            |
| <span data-ttu-id="7f762-120">Defaultframe</span><span class="sxs-lookup"><span data-stu-id="7f762-120">DefaultFrame</span></span>       | <span data-ttu-id="7f762-121">Bestimmt, ob die defaultframe-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-121">Determines whether the defaultFrame property can be set.</span></span>       |
| <span data-ttu-id="7f762-122">Enableerrordialogfelder</span><span class="sxs-lookup"><span data-stu-id="7f762-122">EnableErrorDialogs</span></span> | <span data-ttu-id="7f762-123">Bestimmt, ob die enableerrordialogs-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-123">Determines whether the enableErrorDialogs property can be set.</span></span> |
| <span data-ttu-id="7f762-124">GetMode</span><span class="sxs-lookup"><span data-stu-id="7f762-124">GetMode</span></span>            | <span data-ttu-id="7f762-125">Bestimmt, ob die getMode-Methode aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-125">Determines whether the getMode method can be called.</span></span>           |
| <span data-ttu-id="7f762-126">Invokeurls</span><span class="sxs-lookup"><span data-stu-id="7f762-126">InvokeURLs</span></span>         | <span data-ttu-id="7f762-127">Bestimmt, ob die invokeurls-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-127">Determines whether the invokeURLs property can be set.</span></span>         |
| <span data-ttu-id="7f762-128">Mute</span><span class="sxs-lookup"><span data-stu-id="7f762-128">Mute</span></span>               | <span data-ttu-id="7f762-129">Bestimmt, ob die stumm Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-129">Determines whether the mute property can be set.</span></span>               |
| <span data-ttu-id="7f762-130">Playcount</span><span class="sxs-lookup"><span data-stu-id="7f762-130">PlayCount</span></span>          | <span data-ttu-id="7f762-131">Bestimmt, ob die playcount-Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-131">Determines whether the playCount property can be set.</span></span>          |
| <span data-ttu-id="7f762-132">Rate</span><span class="sxs-lookup"><span data-stu-id="7f762-132">Rate</span></span>               | <span data-ttu-id="7f762-133">Bestimmt, ob die Raten Eigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-133">Determines whether the rate property can be set.</span></span>               |
| <span data-ttu-id="7f762-134">SetMode</span><span class="sxs-lookup"><span data-stu-id="7f762-134">SetMode</span></span>            | <span data-ttu-id="7f762-135">Bestimmt, ob die setmode-Methode aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-135">Determines whether the setMode method can be called.</span></span>           |
| <span data-ttu-id="7f762-136">Lautstärke</span><span class="sxs-lookup"><span data-stu-id="7f762-136">Volume</span></span>             | <span data-ttu-id="7f762-137">Bestimmt, ob die Volumeeigenschaft festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7f762-137">Determines whether the volume property can be set.</span></span>             |



 

## <a name="return-values"></a><span data-ttu-id="7f762-138">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7f762-138">Return Values</span></span>

<span data-ttu-id="7f762-139">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f762-139">This method returns a **Boolean** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f762-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f762-140">Requirements</span></span>



| <span data-ttu-id="7f762-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f762-141">Requirement</span></span> | <span data-ttu-id="7f762-142">Wert</span><span class="sxs-lookup"><span data-stu-id="7f762-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f762-143">Version</span><span class="sxs-lookup"><span data-stu-id="7f762-143">Version</span></span><br/> | <span data-ttu-id="7f762-144">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7f762-144">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7f762-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7f762-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f762-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f762-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f762-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f762-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f762-148">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="7f762-148">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





