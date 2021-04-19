---
title: Controls. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | Controls. IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- Steuerelemente. IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61afa07596a55208be63bd29759fd5f9f3e10170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370204"
---
# <a name="controlsisavailable"></a><span data-ttu-id="53626-105">Controls. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="53626-105">Controls.isAvailable</span></span>

<span data-ttu-id="53626-106">Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="53626-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="53626-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="53626-107">Parameters</span></span>

<span data-ttu-id="53626-108">*name*</span><span class="sxs-lookup"><span data-stu-id="53626-108">*name*</span></span>

<span data-ttu-id="53626-109">Eine **Zeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="53626-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="53626-110">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="53626-110">String</span></span>          | <span data-ttu-id="53626-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53626-111">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53626-112">currentItem</span><span class="sxs-lookup"><span data-stu-id="53626-112">currentItem</span></span>     | <span data-ttu-id="53626-113">Bestimmt, **ob der Benutzer die Eigenschaft "** Eigenschaft" festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="53626-113">Determines whether the user can set the **currentItem** property.</span></span>                                                                                                 |
| <span data-ttu-id="53626-114">currentmarker</span><span class="sxs-lookup"><span data-stu-id="53626-114">currentMarker</span></span>   | <span data-ttu-id="53626-115">Bestimmt, ob der Benutzer einen bestimmten Marker suchen kann.</span><span class="sxs-lookup"><span data-stu-id="53626-115">Determines whether the user can seek to a specific marker.</span></span>                                                                                                        |
| <span data-ttu-id="53626-116">CurrentPosition</span><span class="sxs-lookup"><span data-stu-id="53626-116">currentPosition</span></span> | <span data-ttu-id="53626-117">Bestimmt, ob der Benutzer eine bestimmte Position in der Datei suchen kann.</span><span class="sxs-lookup"><span data-stu-id="53626-117">Determines whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="53626-118">Einige Dateien unterstützen keine Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="53626-118">Some files do not support seeking.</span></span>                                                       |
| <span data-ttu-id="53626-119">FastForward</span><span class="sxs-lookup"><span data-stu-id="53626-119">fastForward</span></span>     | <span data-ttu-id="53626-120">Bestimmt, ob die Datei eine schnelle Weiterleitung unterstützt und ob diese Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="53626-120">Determines whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="53626-121">FastForward wird von vielen Dateitypen (oder Livestreams) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53626-121">Many file types (or live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="53626-122">fastreverse</span><span class="sxs-lookup"><span data-stu-id="53626-122">fastReverse</span></span>     | <span data-ttu-id="53626-123">Bestimmt, ob die Datei fastreverse unterstützt und ob diese Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="53626-123">Determines whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="53626-124">Fastreverse wird von vielen Dateitypen (oder Livestreams) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53626-124">Many file types (or live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="53626-125">Weiter</span><span class="sxs-lookup"><span data-stu-id="53626-125">next</span></span>            | <span data-ttu-id="53626-126">Bestimmt, ob der Benutzer den nächsten Eintrag in einer Wiedergabeliste suchen kann.</span><span class="sxs-lookup"><span data-stu-id="53626-126">Determines whether the user can seek to the next entry in a playlist.</span></span>                                                                                             |
| <span data-ttu-id="53626-127">pause</span><span class="sxs-lookup"><span data-stu-id="53626-127">pause</span></span>           | <span data-ttu-id="53626-128">Bestimmt, ob die **Pause** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="53626-128">Determines whether the **pause** method is available.</span></span>                                                                                                             |
| <span data-ttu-id="53626-129">Theater</span><span class="sxs-lookup"><span data-stu-id="53626-129">play</span></span>            | <span data-ttu-id="53626-130">Bestimmt, ob die **Play** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="53626-130">Determines whether the **play** method is available.</span></span>                                                                                                              |
| <span data-ttu-id="53626-131">Vorherige</span><span class="sxs-lookup"><span data-stu-id="53626-131">previous</span></span>        | <span data-ttu-id="53626-132">Bestimmt, ob der Benutzer den vorherigen Eintrag in einer Wiedergabeliste suchen kann.</span><span class="sxs-lookup"><span data-stu-id="53626-132">Determines whether the user can seek to the previous entry in a playlist.</span></span>                                                                                         |
| <span data-ttu-id="53626-133">Schritt</span><span class="sxs-lookup"><span data-stu-id="53626-133">step</span></span>            | <span data-ttu-id="53626-134">Bestimmt, ob die **Step** -Methode während der Wiedergabe verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="53626-134">Determines whether the **step** method is available during playback.</span></span>                                                                                              |
| <span data-ttu-id="53626-135">stop</span><span class="sxs-lookup"><span data-stu-id="53626-135">stop</span></span>            | <span data-ttu-id="53626-136">Bestimmt, ob die Methode zum **Abbrechen** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="53626-136">Determines whether the **stop** method is available.</span></span>                                                                                                              |



 

## <a name="return-values"></a><span data-ttu-id="53626-137">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="53626-137">Return Values</span></span>

<span data-ttu-id="53626-138">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="53626-138">This method returns a **Boolean** value.</span></span>

## <a name="examples"></a><span data-ttu-id="53626-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53626-139">Examples</span></span>

<span data-ttu-id="53626-140">Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das die Anfangsposition des aktuellen Medien Elements aufsucht.</span><span class="sxs-lookup"><span data-stu-id="53626-140">The following example creates an HTML BUTTON element that seeks to the starting position of the current media item.</span></span> <span data-ttu-id="53626-141">Der JScript-Code verwendet **IsAvailable** , um zu überprüfen, ob die Datei den Suchvorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53626-141">The JScript code uses **isAvailable** to verify that the file supports the seek operation.</span></span> <span data-ttu-id="53626-142">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="53626-142">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a><span data-ttu-id="53626-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53626-143">Requirements</span></span>



| <span data-ttu-id="53626-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53626-144">Requirement</span></span> | <span data-ttu-id="53626-145">Wert</span><span class="sxs-lookup"><span data-stu-id="53626-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53626-146">Version</span><span class="sxs-lookup"><span data-stu-id="53626-146">Version</span></span><br/> | <span data-ttu-id="53626-147">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="53626-147">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="53626-148">DLL</span><span class="sxs-lookup"><span data-stu-id="53626-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="53626-149"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53626-149"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53626-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53626-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53626-151">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="53626-151">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





