---
title: IAgentCharacter Prepare
description: IAgentCharacter Prepare
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119875"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="1720a-103">IAgentCharacter::P repare</span><span class="sxs-lookup"><span data-stu-id="1720a-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="1720a-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="1720a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="1720a-105">Ruft Animationsdaten für ein Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="1720a-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1720a-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="1720a-107">Wenn die Funktion zurückgegeben wird, enthält *pdwReqID* die ID der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="1720a-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="1720a-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="1720a-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="1720a-109">Ein -Wert, der den zu ladenden Animationsdatentyp angibt, der einer der folgenden Sein muss:</span><span class="sxs-lookup"><span data-stu-id="1720a-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="1720a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1720a-110">Value</span></span>                                                           | <span data-ttu-id="1720a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1720a-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="1720a-112">**const unsigned short** **PREPARE ANIMATION = \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="1720a-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="1720a-113">Animationsdaten eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1720a-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="1720a-114">**const unsigned short** **PREPARE STATE = \_ 1;**</span><span class="sxs-lookup"><span data-stu-id="1720a-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="1720a-115">Zustandsdaten eines Zeichens.</span><span class="sxs-lookup"><span data-stu-id="1720a-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="1720a-116">**const unsigned short** **PREPARE WAVE = \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1720a-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="1720a-117">Die Sounddatei eines Zeichens (. WAV oder . LWV) für die gesprochene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1720a-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1720a-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="1720a-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="1720a-119">Der Name der Animation oder des Zustands.</span><span class="sxs-lookup"><span data-stu-id="1720a-119">The name of the animation or state.</span></span>

<span data-ttu-id="1720a-120">Der Animationsname basiert auf dem Namen, der für das Zeichen definiert wurde, als es mit dem Microsoft-Agent-Zeichen-Editor gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="1720a-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="1720a-121">Für Status kann der Wert einer der folgenden Sein:</span><span class="sxs-lookup"><span data-stu-id="1720a-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="1720a-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1720a-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="1720a-123">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="1720a-123">**"Gesturing"**</span></span>      | <span data-ttu-id="1720a-124">So rufen Sie alle **Gesturingzustandsanimationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="1720a-125">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="1720a-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="1720a-126">So rufen Sie **GesturingDown-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="1720a-127">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="1720a-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="1720a-128">So rufen Sie **GesturingLeft-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="1720a-129">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="1720a-129">**"GesturingRight"**</span></span> | <span data-ttu-id="1720a-130">So rufen Sie **GesturingRight-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="1720a-131">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="1720a-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="1720a-132">So rufen Sie **GesturingUp-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="1720a-133">**"Ausblenden"**</span><span class="sxs-lookup"><span data-stu-id="1720a-133">**"Hiding"**</span></span>         | <span data-ttu-id="1720a-134">So rufen Sie die Animationen des **Ausblendenszustands** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="1720a-135">**"Hörvermögen"**</span><span class="sxs-lookup"><span data-stu-id="1720a-135">**"Hearing"**</span></span>        | <span data-ttu-id="1720a-136">So rufen  Sie die Hörzustandsanimationen ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="1720a-137">**"Idling"**</span><span class="sxs-lookup"><span data-stu-id="1720a-137">**"Idling"**</span></span>         | <span data-ttu-id="1720a-138">So rufen  Sie alle Idling-Zustandsanimationen ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="1720a-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="1720a-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="1720a-140">So rufen Sie alle **IdlingLevel1-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="1720a-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="1720a-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="1720a-142">So rufen Sie alle **IdlingLevel2-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="1720a-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="1720a-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="1720a-144">So rufen Sie alle **IdlingLevel3-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="1720a-145">**"Lauschen"**</span><span class="sxs-lookup"><span data-stu-id="1720a-145">**"Listening"**</span></span>      | <span data-ttu-id="1720a-146">So rufen  Sie die Überwachungzustandsanimationen ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="1720a-147">**"Moving" (Verschieben)**</span><span class="sxs-lookup"><span data-stu-id="1720a-147">**"Moving"**</span></span>         | <span data-ttu-id="1720a-148">So rufen Sie alle **Animationen des Bewegungszustands** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="1720a-149">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="1720a-149">**"MovingDown"**</span></span>     | <span data-ttu-id="1720a-150">So rufen Sie alle **Moving-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="1720a-151">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="1720a-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="1720a-152">So rufen Sie alle **MovingLeft-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="1720a-153">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="1720a-153">**"MovingRight"**</span></span>    | <span data-ttu-id="1720a-154">So rufen Sie alle **MovingRight-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="1720a-155">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="1720a-155">**"MovingUp"**</span></span>       | <span data-ttu-id="1720a-156">So rufen Sie alle **MovingUp-Animationen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="1720a-157">**"Showing" (Wird angezeigt)**</span><span class="sxs-lookup"><span data-stu-id="1720a-157">**"Showing"**</span></span>        | <span data-ttu-id="1720a-158">So rufen Sie die **Zustandsanimationen anzeigen** ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="1720a-159">**"Sprechen"**</span><span class="sxs-lookup"><span data-stu-id="1720a-159">**"Speaking"**</span></span>       | <span data-ttu-id="1720a-160">So rufen  Sie die Sprechzustandsanimationen ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="1720a-161">Für. WAV-Dateien: Legen Sie *bszName* auf die URL oder Dateispezifikation für fest. WAV-Datei.</span><span class="sxs-lookup"><span data-stu-id="1720a-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="1720a-162">Wenn die Spezifikation nicht vollständig ist, wird sie als relativ zur Spezifikation interpretiert, die in der [**Load-Methode**](https://www.bing.com/search?q=**Load**) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1720a-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="1720a-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="1720a-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="1720a-164">Ein boolescher Wert, der angibt, ob der Server die [**Prepare-Anforderung**](/windows/desktop/lwef/iagentcharacter--prepare) in die Warteschlange stellt.</span><span class="sxs-lookup"><span data-stu-id="1720a-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="1720a-165">**True** stellt die Anforderung in die Warteschlange und bewirkt, dass jede darauf folgende Animationsanforderung wartet, bis die von ihr angegebenen Animationsdaten geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1720a-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="1720a-166">**False** ruft die Animationsdaten asynchron ab.</span><span class="sxs-lookup"><span data-stu-id="1720a-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="1720a-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="1720a-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="1720a-168">Adresse einer Variablen, die die Anforderungs-ID [**vorbereiten**](/windows/desktop/lwef/iagentcharacter--prepare) empfängt.</span><span class="sxs-lookup"><span data-stu-id="1720a-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="1720a-169">Wenn Sie ein Zeichen mithilfe des HTTP-Protokolls laden (ein . ACF-Datei), müssen Sie die [**Prepare-Methode**](/windows/desktop/lwef/iagentcharacter--prepare) verwenden, um Animationsdaten abzurufen, bevor Sie die Animation wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="1720a-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="1720a-170">Sie können diese Methode nicht verwenden, wenn Sie das Zeichen mit dem UNC-Protokoll (einem ) geladen haben. ACS-Datei).</span><span class="sxs-lookup"><span data-stu-id="1720a-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="1720a-171">Sie können mit **Prepare** auch keine HTTP-Daten für ein Zeichen abrufen, wenn Sie dieses Zeichen mithilfe des UNC-Protokolls geladen haben (. ACS-Zeichendatei).</span><span class="sxs-lookup"><span data-stu-id="1720a-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="1720a-172">Mit der [**Prepare-Methode**](/windows/desktop/lwef/iagentcharacter--prepare) abgerufene Animations- oder Sounddaten werden im Cache des Browsers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1720a-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="1720a-173">Nachfolgende Aufrufe überprüfen den Cache, und wenn die Animationsdaten bereits vorhanden sind, lädt das Steuerelement die Daten direkt aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="1720a-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="1720a-174">Nach dem Laden können die Animations- oder Sounddaten mit den [**Methoden Wiedergeben**](/windows/desktop/lwef/iagentcharacter--play) oder [**Sprechen**](/windows/desktop/lwef/iagentcharacter--speak) wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1720a-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="1720a-175">Sie können mehrere Animationen und Zustände angeben, indem Sie sie durch Kommas trennen.</span><span class="sxs-lookup"><span data-stu-id="1720a-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="1720a-176">Sie können Typen jedoch nicht in derselben [**Prepare-Anweisung**](/windows/desktop/lwef/iagentcharacter--prepare) mischen.</span><span class="sxs-lookup"><span data-stu-id="1720a-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

