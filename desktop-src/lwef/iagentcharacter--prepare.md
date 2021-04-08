---
title: Iagentcharacter-Vorbereitung
description: Iagentcharacter-Vorbereitung
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038956"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="3cd1e-103">Iagentcharacter::P repare</span><span class="sxs-lookup"><span data-stu-id="3cd1e-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="3cd1e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="3cd1e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="3cd1e-105">Ruft Animationsdaten für ein Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="3cd1e-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="3cd1e-107">Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="3cd1e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="3cd1e-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="3cd1e-109">Ein Wert, der den zu ladenden Animations Datentyp angibt, der eines der folgenden sein muss:</span><span class="sxs-lookup"><span data-stu-id="3cd1e-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="3cd1e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="3cd1e-110">Value</span></span>                                                           | <span data-ttu-id="3cd1e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3cd1e-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3cd1e-112">Animation für " **Ganzzahl ohne Vorzeichen Short** **Prepare" \_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="3cd1e-113">Die Animationsdaten eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="3cd1e-114">**Ganzzahl ohne Vorzeichen Short** **Prepare \_ State = 1;**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="3cd1e-115">Die Zustandsdaten eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="3cd1e-116">Konstante " **Ganzzahl ohne Vorzeichen Short** **Prepare \_ Wave = 2** "</span><span class="sxs-lookup"><span data-stu-id="3cd1e-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="3cd1e-117">Die Audiodatei eines Zeichens (. WAV oder. Lwv) für die gesprochene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3cd1e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszname*</span><span class="sxs-lookup"><span data-stu-id="3cd1e-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="3cd1e-119">Der Name der Animation oder des Zustands.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-119">The name of the animation or state.</span></span>

<span data-ttu-id="3cd1e-120">Der Animations Name basiert auf dem, der für das Zeichen definiert wurde, als es mit dem Microsoft-Agent-Zeichen-Editor gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="3cd1e-121">Für Zustände kann der Wert eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="3cd1e-121">For states, the value can be one of the following:</span></span>



|                      |                                                 |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="3cd1e-122">**"Gesturung"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-122">**"Gesturing"**</span></span>      | <span data-ttu-id="3cd1e-123">Zum Abrufen aller **gestörenden** Zustands Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-123">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="3cd1e-124">**"Gesturingdown"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-124">**"GesturingDown"**</span></span>  | <span data-ttu-id="3cd1e-125">Zum Abrufen von **gesturingdown** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-125">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="3cd1e-126">**"Gesturingleft"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-126">**"GesturingLeft"**</span></span>  | <span data-ttu-id="3cd1e-127">Zum Abrufen von **gesturingleft** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-127">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="3cd1e-128">**"Gesturingright"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-128">**"GesturingRight"**</span></span> | <span data-ttu-id="3cd1e-129">Zum Abrufen von **gesturingright** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-129">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="3cd1e-130">**"Gesturingup"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-130">**"GesturingUp"**</span></span>    | <span data-ttu-id="3cd1e-131">Zum Abrufen von **gesturingup** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-131">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="3cd1e-132">**Zieher**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-132">**"Hiding"**</span></span>         | <span data-ttu-id="3cd1e-133">Zum **Abrufen der Animationen zum Ausblenden** des Zustands.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-133">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="3cd1e-134">**Sinn**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-134">**"Hearing"**</span></span>        | <span data-ttu-id="3cd1e-135">Zum Abrufen der **hörzustands** Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-135">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="3cd1e-136">**Leerlauf**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-136">**"Idling"**</span></span>         | <span data-ttu-id="3cd1e-137">, Um alle **idck** State-Animationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-137">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="3cd1e-138">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-138">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="3cd1e-139">Zum Abrufen aller **IdlingLevel1** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-139">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="3cd1e-140">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-140">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="3cd1e-141">Zum Abrufen aller **IdlingLevel2** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-141">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="3cd1e-142">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-142">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="3cd1e-143">Zum Abrufen aller **IdlingLevel3** -Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-143">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="3cd1e-144">**Raum**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-144">**"Listening"**</span></span>      | <span data-ttu-id="3cd1e-145">**Zum Abrufen der Animation** des Empfangs Zustands.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-145">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="3cd1e-146">**Verschieben**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-146">**"Moving"**</span></span>         | <span data-ttu-id="3cd1e-147">Zum Abrufen aller **beweglicher** Zustands Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-147">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="3cd1e-148">**""**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-148">**"MovingDown"**</span></span>     | <span data-ttu-id="3cd1e-149">, Um alle Verschieb **enden** Animationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-149">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="3cd1e-150">**"Wvingleft"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-150">**"MovingLeft"**</span></span>     | <span data-ttu-id="3cd1e-151">Zum Abrufen aller Animationen von " **wvingleft** ".</span><span class="sxs-lookup"><span data-stu-id="3cd1e-151">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="3cd1e-152">**"Wvingright"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-152">**"MovingRight"**</span></span>    | <span data-ttu-id="3cd1e-153">, Um alle **wvingright** -Animationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-153">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="3cd1e-154">**"Wvingup"**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-154">**"MovingUp"**</span></span>       | <span data-ttu-id="3cd1e-155">Zum Abrufen aller " **wvingup** "-Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-155">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="3cd1e-156">**Zeigten**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-156">**"Showing"**</span></span>        | <span data-ttu-id="3cd1e-157">Zum Abrufen der **Anzeige** Zustands Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-157">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="3cd1e-158">**Isch**</span><span class="sxs-lookup"><span data-stu-id="3cd1e-158">**"Speaking"**</span></span>       | <span data-ttu-id="3cd1e-159">Zum Abrufen der **sprach** Zustands Animationen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-159">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="3cd1e-160">Damit. WAV-Dateien, legen Sie *bszname* auf die URL oder die Datei Spezifikation für fest. WAV-Datei.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-160">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="3cd1e-161">Wenn die Spezifikation nicht fertig ist, wird Sie als relativ zu der in der [**Load**](https://www.bing.com/search?q=**Load**) -Methode verwendeten Spezifikation interpretiert.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-161">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="3cd1e-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bqueue*</span><span class="sxs-lookup"><span data-stu-id="3cd1e-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="3cd1e-163">Ein boolescher Wert, der angibt, ob der Server die [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Anforderung anfügt.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-163">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="3cd1e-164">**True** fügt die Anforderung in die Warteschlange ein und bewirkt, dass alle darauf folgenden Animations Anforderungen warten, bis die von ihr festgelegten Animationsdaten geladen sind.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-164">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="3cd1e-165">**False** Ruft die Animationsdaten asynchron ab.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-165">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="3cd1e-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="3cd1e-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="3cd1e-167">Adresse einer Variablen, die die ID der [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-167">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="3cd1e-168">Wenn Sie ein Zeichen mithilfe des HTTP-Protokolls (ein-Zeichen) laden. ACF-Datei). Sie müssen die [**Vorbereitungs**](/windows/desktop/lwef/iagentcharacter--prepare) Methode zum Abrufen von Animationsdaten verwenden, bevor Sie die Animation wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-168">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="3cd1e-169">Diese Methode kann nicht verwendet werden, wenn Sie das Zeichen mithilfe des UNC-Protokolls (eines geladen haben. ACS-Datei).</span><span class="sxs-lookup"><span data-stu-id="3cd1e-169">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="3cd1e-170">Sie können auch keine HTTP-Daten für ein Zeichen abrufen, indem Sie **vorbereiten** verwenden, wenn Sie dieses Zeichen mithilfe des UNC-Protokolls () geladen haben. ACS-Zeichen Datei).</span><span class="sxs-lookup"><span data-stu-id="3cd1e-170">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="3cd1e-171">Die mit der [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode abgerufenen Animations-oder Audiodaten werden im Cache des Browsers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-171">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="3cd1e-172">Bei nachfolgenden Aufrufen wird der Cache überprüft. wenn die Animationsdaten bereits vorhanden sind, lädt das-Steuerelement die Daten direkt aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-172">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="3cd1e-173">Nach dem Laden können die Animations-oder Audiodaten mit den Methoden " [**abspielen**](/windows/desktop/lwef/iagentcharacter--play) " und " [**Sprache**](/windows/desktop/lwef/iagentcharacter--speak) " wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-173">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="3cd1e-174">Sie können mehrere Animationen und Zustände angeben, indem Sie Sie durch Kommas trennen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-174">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="3cd1e-175">Es ist jedoch nicht möglich, Typen in derselben [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Anweisung zu mischen.</span><span class="sxs-lookup"><span data-stu-id="3cd1e-175">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

