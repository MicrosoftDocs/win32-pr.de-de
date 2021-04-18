---
title: Player. ScriptCommand-Ereignis
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | Player. ScriptCommand-Ereignis
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand-Ereignisfenster Media Player
- ScriptCommand-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, ScriptCommand-Ereignis
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365856"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="7524b-107">Player. ScriptCommand-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7524b-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="7524b-108">Das **ScriptCommand** -Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="7524b-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="7524b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7524b-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="7524b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7524b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7524b-111">*sctype*</span><span class="sxs-lookup"><span data-stu-id="7524b-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="7524b-112">Zeichenfolge, die den Typ des Skript Befehls angibt.</span><span class="sxs-lookup"><span data-stu-id="7524b-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="7524b-113">*Parameter*</span><span class="sxs-lookup"><span data-stu-id="7524b-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="7524b-114">**Zeichenfolge** , die den Skript Befehl angibt.</span><span class="sxs-lookup"><span data-stu-id="7524b-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7524b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7524b-115">Return value</span></span>

<span data-ttu-id="7524b-116">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7524b-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7524b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7524b-117">Remarks</span></span>

<span data-ttu-id="7524b-118">Befehle können zwischen den Sounds und Bildern einer Windows Media-Datei oder eines Windows-Streams eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="7524b-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="7524b-119">Die Befehle sind ein paar von Unicode-Zeichen folgen, die mit einer bestimmten Zeit im Stream verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7524b-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="7524b-120">Wenn der Stream den dem Befehl zugeordneten Zeitpunkt erreicht, sendet das Windows Media Player-Steuerelement ein **ScriptCommand** -Ereignis mit zwei Parametern.</span><span class="sxs-lookup"><span data-stu-id="7524b-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="7524b-121">Ein Parameter gibt den Typ des gesendeten Befehls an, und der andere Parameter gibt den Befehl an.</span><span class="sxs-lookup"><span data-stu-id="7524b-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="7524b-122">Der Parametertyp wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="7524b-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="7524b-123">Alle Befehls Typen können in eine Datei oder einen Stream eingebettet werden, damit Sie vom **ScriptCommand** -Ereignis verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="7524b-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7524b-124">In der folgenden Tabelle sind Skript Befehls Typen aufgeführt, die automatisch von Windows Media Player verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="7524b-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="7524b-125">type</span><span class="sxs-lookup"><span data-stu-id="7524b-125">Type</span></span>                   | <span data-ttu-id="7524b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7524b-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7524b-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="7524b-127">CAPTION</span></span>                | <span data-ttu-id="7524b-128">Das-Steuerelement zeigt den zugeordneten Text in dem durch *closedcaption* angegebenen div-Element an. **captioningid**.</span><span class="sxs-lookup"><span data-stu-id="7524b-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="7524b-129">EREIGNIS</span><span class="sxs-lookup"><span data-stu-id="7524b-129">EVENT</span></span>                  | <span data-ttu-id="7524b-130">Weist das Steuerelement an, Anweisungen auszuführen, die für das angegebene Ereignis definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7524b-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="7524b-131">Einfügen</span><span class="sxs-lookup"><span data-stu-id="7524b-131">FILENAME</span></span>               | <span data-ttu-id="7524b-132">Das-Steuerelement setzt seine **URL** -Eigenschaft zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.</span><span class="sxs-lookup"><span data-stu-id="7524b-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="7524b-133">OpenEvent</span><span class="sxs-lookup"><span data-stu-id="7524b-133">OPENEVENT</span></span>              | <span data-ttu-id="7524b-134">Puffert den zugeordneten Ereignistyp Befehl für die rechtzeitige Ausführung des Ereignis Skripts.</span><span class="sxs-lookup"><span data-stu-id="7524b-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="7524b-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="7524b-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="7524b-136">Der Parameter *param* enthält den synchronisierten Text.</span><span class="sxs-lookup"><span data-stu-id="7524b-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="7524b-137">In Windows Media Player wird der Text im Bereich geschlossene Überschrift der Funktion **jetzt abgespielt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7524b-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="7524b-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="7524b-138">TEXT</span></span>                   | <span data-ttu-id="7524b-139">Das-Steuerelement zeigt den zugeordneten Text in dem durch *closedcaption* angegebenen div-Element an. **captioningid**.</span><span class="sxs-lookup"><span data-stu-id="7524b-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="7524b-140">URL</span><span class="sxs-lookup"><span data-stu-id="7524b-140">URL</span></span>                    | <span data-ttu-id="7524b-141">Das-Steuerelement öffnet automatisch die URL, die mit dem Standard Internet Browser angegeben wird, wenn die *Einstellungen*. die **invokeurls** -Eigenschaft ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7524b-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="7524b-142">Sie können beliebige andere Befehls Typen einbetten, solange Sie gegenseitigen Code zur Behandlung des Befehls bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7524b-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="7524b-143">Obwohl unbekannte Befehle vom Windows Media Player-Steuerelement ignoriert werden, werden Sie weiterhin an das **ScriptCommand** -Ereignis übergeben.</span><span class="sxs-lookup"><span data-stu-id="7524b-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="7524b-144">URL-Befehle, die vom Windows Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standard Webbrowser aufgerufen, wenn die *Einstellungen*. die **invokeurls** -Eigenschaft ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7524b-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="7524b-145">Sie können die *Einstellungen* verwenden. **defaultframe** -Eigenschaft, um den Zielframe anzugeben, in dem die Webseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7524b-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="7524b-146">Die an Windows Media Player gesendete URL wird relativ zur Basis-URL verarbeitet, die in den *Einstellungen* angegeben ist. **baseurl** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7524b-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="7524b-147">Die Basis-URL wird mit der relativ angegebenen URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7524b-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="7524b-148">Das Windows Media Player-Steuerelement verarbeitet eingehende URL-Typbefehle immer wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7524b-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="7524b-149">Ein URL-Type-Befehl wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="7524b-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="7524b-150">*Einstellungen*. **baseurl** wird verwendet, um eine vollständige URL aus der relative URL zu erstellen, die im Skript Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7524b-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="7524b-151">*ScriptCommand* wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7524b-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="7524b-152">Nachdem *ScriptCommand* zurückgegeben wurde, werden die *Einstellungen*. **invokeurls** wird geprüft.</span><span class="sxs-lookup"><span data-stu-id="7524b-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="7524b-153">Wenn *Einstellungen*. **invokeurls** ist true, und der Befehl ist ein URL-Typ, die angegebene URL wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7524b-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="7524b-154">Wenn *Einstellungen*. **invokeurls** ist false, oder wenn der Befehl kein URL-Typ ist, wird der Befehl ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7524b-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="7524b-155">Wenn Sie eine Windows Media-Datei erstellen, können Sie angeben, in welchem Frame die neue URL angezeigt werden soll, indem Sie zwei kaufmännische und den Namen des Frames im Parameterfeld verketten.</span><span class="sxs-lookup"><span data-stu-id="7524b-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="7524b-156">Im folgenden Beispiel werden typische *ScriptCommand* -Parameter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7524b-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="7524b-157">Er gibt an, dass die URL *MyPage* im Frame " *MyFrame* " gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="7524b-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="7524b-158">Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnell weitergeleitet oder schnell-umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="7524b-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="7524b-159">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="7524b-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="7524b-160">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="7524b-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="7524b-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7524b-161">Requirements</span></span>



| <span data-ttu-id="7524b-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7524b-162">Requirement</span></span> | <span data-ttu-id="7524b-163">Wert</span><span class="sxs-lookup"><span data-stu-id="7524b-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7524b-164">Version</span><span class="sxs-lookup"><span data-stu-id="7524b-164">Version</span></span><br/> | <span data-ttu-id="7524b-165">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7524b-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7524b-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7524b-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="7524b-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7524b-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7524b-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7524b-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7524b-169">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7524b-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="7524b-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7524b-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="7524b-171">**Settings. baseurl**</span><span class="sxs-lookup"><span data-stu-id="7524b-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="7524b-172">**Settings. defaultframe**</span><span class="sxs-lookup"><span data-stu-id="7524b-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="7524b-173">**Settings. invokeurls**</span><span class="sxs-lookup"><span data-stu-id="7524b-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





