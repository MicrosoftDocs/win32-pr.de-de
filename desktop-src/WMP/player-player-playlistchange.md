---
title: Player. playlistchange-Ereignis
description: Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird. | Player. playlistchange-Ereignis
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player "playlistchange-Ereignisfenster"
- Playlistchange-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, playlistchange-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360363"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="a43fd-107">Player. playlistchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a43fd-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="a43fd-108">Das **playlistchange** -Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a43fd-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43fd-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="a43fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a43fd-111">*Abspielen*</span><span class="sxs-lookup"><span data-stu-id="a43fd-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="a43fd-112">**Wiedergabe** Listen Objekt, das geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a43fd-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="a43fd-113">*change*</span><span class="sxs-lookup"><span data-stu-id="a43fd-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="a43fd-114">**Zahl** (**Long**), die den Typ der Änderung angibt, die in der Wiedergabeliste aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a43fd-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="a43fd-115">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="a43fd-115">Contains one of the following values.</span></span>



| <span data-ttu-id="a43fd-116">number</span><span class="sxs-lookup"><span data-stu-id="a43fd-116">Number</span></span> | <span data-ttu-id="a43fd-117">name</span><span class="sxs-lookup"><span data-stu-id="a43fd-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="a43fd-118">0</span><span class="sxs-lookup"><span data-stu-id="a43fd-118">0</span></span>      | <span data-ttu-id="a43fd-119">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="a43fd-119">Unknown</span></span>       |
| <span data-ttu-id="a43fd-120">1</span><span class="sxs-lookup"><span data-stu-id="a43fd-120">1</span></span>      | <span data-ttu-id="a43fd-121">Clear</span><span class="sxs-lookup"><span data-stu-id="a43fd-121">Clear</span></span>         |
| <span data-ttu-id="a43fd-122">2</span><span class="sxs-lookup"><span data-stu-id="a43fd-122">2</span></span>      | <span data-ttu-id="a43fd-123">Infochange</span><span class="sxs-lookup"><span data-stu-id="a43fd-123">InfoChange</span></span>    |
| <span data-ttu-id="a43fd-124">3</span><span class="sxs-lookup"><span data-stu-id="a43fd-124">3</span></span>      | <span data-ttu-id="a43fd-125">Move</span><span class="sxs-lookup"><span data-stu-id="a43fd-125">Move</span></span>          |
| <span data-ttu-id="a43fd-126">4</span><span class="sxs-lookup"><span data-stu-id="a43fd-126">4</span></span>      | <span data-ttu-id="a43fd-127">Löschen</span><span class="sxs-lookup"><span data-stu-id="a43fd-127">Delete</span></span>        |
| <span data-ttu-id="a43fd-128">5</span><span class="sxs-lookup"><span data-stu-id="a43fd-128">5</span></span>      | <span data-ttu-id="a43fd-129">Einfügen</span><span class="sxs-lookup"><span data-stu-id="a43fd-129">Insert</span></span>        |
| <span data-ttu-id="a43fd-130">6</span><span class="sxs-lookup"><span data-stu-id="a43fd-130">6</span></span>      | <span data-ttu-id="a43fd-131">Anfügen</span><span class="sxs-lookup"><span data-stu-id="a43fd-131">Append</span></span>        |
| <span data-ttu-id="a43fd-132">7</span><span class="sxs-lookup"><span data-stu-id="a43fd-132">7</span></span>      | <span data-ttu-id="a43fd-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a43fd-133">Not supported</span></span> |
| <span data-ttu-id="a43fd-134">8</span><span class="sxs-lookup"><span data-stu-id="a43fd-134">8</span></span>      | <span data-ttu-id="a43fd-135">Name Change</span><span class="sxs-lookup"><span data-stu-id="a43fd-135">NameChange</span></span>    |
| <span data-ttu-id="a43fd-136">9</span><span class="sxs-lookup"><span data-stu-id="a43fd-136">9</span></span>      | <span data-ttu-id="a43fd-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a43fd-137">Not supported</span></span> |
| <span data-ttu-id="a43fd-138">10</span><span class="sxs-lookup"><span data-stu-id="a43fd-138">10</span></span>     | <span data-ttu-id="a43fd-139">Sortieren</span><span class="sxs-lookup"><span data-stu-id="a43fd-139">Sort</span></span>          |



 

<span data-ttu-id="a43fd-140">Die Enumerationskonstante im C-Stil kann durch Voranstellen des Namens Werts mit "wmsps" abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a43fd-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="a43fd-141">Beispielsweise ist die Konstante für den Verschiebungs Zustand **wmplcmove**.</span><span class="sxs-lookup"><span data-stu-id="a43fd-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a43fd-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a43fd-142">Return value</span></span>

<span data-ttu-id="a43fd-143">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a43fd-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a43fd-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a43fd-144">Remarks</span></span>

<span data-ttu-id="a43fd-145">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="a43fd-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="a43fd-146">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="a43fd-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="a43fd-147">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a43fd-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a43fd-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a43fd-148">Requirements</span></span>



| <span data-ttu-id="a43fd-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a43fd-149">Requirement</span></span> | <span data-ttu-id="a43fd-150">Wert</span><span class="sxs-lookup"><span data-stu-id="a43fd-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a43fd-151">Version</span><span class="sxs-lookup"><span data-stu-id="a43fd-151">Version</span></span><br/> | <span data-ttu-id="a43fd-152">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a43fd-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a43fd-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a43fd-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="a43fd-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a43fd-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43fd-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a43fd-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43fd-156">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a43fd-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





