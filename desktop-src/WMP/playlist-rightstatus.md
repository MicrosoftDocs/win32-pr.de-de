---
title: Wiedergabeliste. rightstatus
description: Das rightstatus-Attribut gibt den Text an, der auf der rechten und unteren Rand des Wiedergabelisten Elements angezeigt wird, oder ruft diesen ab.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Wiedergabeliste. rightstatus-Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366968"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="47701-104">Wiedergabeliste. rightstatus</span><span class="sxs-lookup"><span data-stu-id="47701-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="47701-105">Das **rightstatus** -Attribut gibt den Text an, der auf der rechten und unteren Rand des **Wiedergabe** Listen Elements angezeigt wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="47701-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="47701-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="47701-106">Possible Values</span></span>

<span data-ttu-id="47701-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="47701-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47701-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47701-108">Remarks</span></span>

<span data-ttu-id="47701-109">Dieses Attribut kann beliebigen Text mit bestimmten Schlüsselwörtern kombinieren, die die gewünschten Informationen anzeigen, z. b. die Gesamtdauer der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="47701-110">Die Schlüsselwörter sind von Prozentzeichen (%) umgeben. , wenn Sie sich vom normalen Text unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="47701-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="47701-111">Die folgenden Schlüsselwörter können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47701-111">The following keywords can be used.</span></span>



| <span data-ttu-id="47701-112">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="47701-112">Keyword</span></span>               | <span data-ttu-id="47701-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47701-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47701-114">count</span><span class="sxs-lookup"><span data-stu-id="47701-114">count</span></span>                 | <span data-ttu-id="47701-115">Anzahl der Elemente in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="47701-116">Größe</span><span class="sxs-lookup"><span data-stu-id="47701-116">size</span></span>                  | <span data-ttu-id="47701-117">Gesamtgröße der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="47701-118">duration</span><span class="sxs-lookup"><span data-stu-id="47701-118">duration</span></span>              | <span data-ttu-id="47701-119">Gesamtdauer der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="47701-120">*XXX*</span><span class="sxs-lookup"><span data-stu-id="47701-120">*XXX*</span></span>                 | <span data-ttu-id="47701-121">Führt ein **getiteminfo** -Element auf der Wiedergabeliste mit *xxx* als Element aus, das empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="47701-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="47701-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="47701-122">SelectedSize</span></span>          | <span data-ttu-id="47701-123">Gesamtgröße der ausgewählten Einträge in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="47701-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="47701-124">SelectedCount</span></span>         | <span data-ttu-id="47701-125">Die Gesamtanzahl der ausgewählten Einträge in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="47701-126">Selectedduration</span><span class="sxs-lookup"><span data-stu-id="47701-126">SelectedDuration</span></span>      | <span data-ttu-id="47701-127">Gesamtdauer der ausgewählten Einträge in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="47701-128">Checkedcount</span><span class="sxs-lookup"><span data-stu-id="47701-128">CheckedCount</span></span>          | <span data-ttu-id="47701-129">Die Gesamtanzahl der überprüften Titel in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="47701-130">Checkedduration</span><span class="sxs-lookup"><span data-stu-id="47701-130">CheckedDuration</span></span>       | <span data-ttu-id="47701-131">Gesamtdauer der aktivierten Titel in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="47701-132">Checkedsize</span><span class="sxs-lookup"><span data-stu-id="47701-132">CheckedSize</span></span>           | <span data-ttu-id="47701-133">Gesamtgröße der aktivierten Titel in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="47701-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="47701-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="47701-134">DurationString</span></span>        | <span data-ttu-id="47701-135">Zeigt Text an, der die Dauer in Abhängigkeit davon, ob die Gesamtwerte bekannt sind, als "Gesamtzeit" oder "geschätzte Zeit" beschreibt.</span><span class="sxs-lookup"><span data-stu-id="47701-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="47701-136">Auf diesen Text folgt "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="47701-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="47701-137">Checkeddurationstring</span><span class="sxs-lookup"><span data-stu-id="47701-137">CheckedDurationString</span></span> | <span data-ttu-id="47701-138">Zeigt Text an, der die Dauer für alle aktivierten Elemente in der Wiedergabeliste als "gesamte Zeit" oder "geschätzte Zeit" beschreibt, abhängig davon, ob die Gesamtwerte bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="47701-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="47701-139">Auf diesen Text folgt "% Duration%".</span><span class="sxs-lookup"><span data-stu-id="47701-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="47701-140">Der Wert "Gesamtzeit:% Duration%" für eine Wiedergabeliste, die eine Gesamtdauer von sieben Minuten enthält, wird "Gesamtzeit: 07:00" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47701-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="47701-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47701-141">Requirements</span></span>



| <span data-ttu-id="47701-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47701-142">Requirement</span></span> | <span data-ttu-id="47701-143">Wert</span><span class="sxs-lookup"><span data-stu-id="47701-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="47701-144">Version</span><span class="sxs-lookup"><span data-stu-id="47701-144">Version</span></span><br/> | <span data-ttu-id="47701-145">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="47701-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47701-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47701-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47701-147">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="47701-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





