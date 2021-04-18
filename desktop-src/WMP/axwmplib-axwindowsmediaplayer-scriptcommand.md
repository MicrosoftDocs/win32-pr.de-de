---
title: ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird. | ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- ScriptCommand-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358093"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="6c591-105">ScriptCommand-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="6c591-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="6c591-106">Das ScriptCommand-Ereignis tritt auf, wenn ein synchronisierter Befehl oder eine synchronisierte URL empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="6c591-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="6c591-107">Event Data</span></span>

<span data-ttu-id="6c591-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ scriptcommandeventhandler**.</span><span class="sxs-lookup"><span data-stu-id="6c591-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="6c591-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ scriptcommandevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6c591-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="6c591-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c591-110">Property</span></span> | <span data-ttu-id="6c591-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c591-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="6c591-112">sctype</span><span class="sxs-lookup"><span data-stu-id="6c591-112">scType</span></span>   | <span data-ttu-id="6c591-113">System. StringGibt den Typ des Skript Befehls an.</span><span class="sxs-lookup"><span data-stu-id="6c591-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="6c591-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c591-114">param</span></span>    | <span data-ttu-id="6c591-115">System. StringGibt den Skript Befehl an.</span><span class="sxs-lookup"><span data-stu-id="6c591-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="6c591-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c591-116">Remarks</span></span>

<span data-ttu-id="6c591-117">Befehle können zwischen den Sounds und Bildern einer Windows Media-Datei oder eines Windows-Streams eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="6c591-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="6c591-118">Die Befehle sind ein paar von Unicode-Zeichen folgen, die mit einer bestimmten Zeit im Stream verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6c591-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="6c591-119">Wenn der Stream den dem Befehl zugeordneten Zeitpunkt erreicht, sendet das Windows Media Player-Steuerelement ein **ScriptCommand** -Ereignis mit zwei Parametern.</span><span class="sxs-lookup"><span data-stu-id="6c591-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="6c591-120">Ein Parameter gibt den Typ des gesendeten Befehls an, und der andere Parameter gibt den Befehl an.</span><span class="sxs-lookup"><span data-stu-id="6c591-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="6c591-121">Der Parametertyp wird verwendet, um zu bestimmen, wie der Befehlsparameter verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="6c591-122">Alle Befehls Typen können in eine Datei oder einen Stream eingebettet werden, damit Sie vom **ScriptCommand** -Ereignis verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="6c591-123">In der folgenden Tabelle sind Skript Befehls Typen aufgeführt, die automatisch von Windows Media Player verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6c591-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="6c591-124">type</span><span class="sxs-lookup"><span data-stu-id="6c591-124">Type</span></span>                   | <span data-ttu-id="6c591-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c591-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c591-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="6c591-126">CAPTION</span></span>                | <span data-ttu-id="6c591-127">Das-Steuerelement zeigt den zugeordneten Text im von iwmpclosedcaption angegebenen HTML-Element an. **captioningid**.</span><span class="sxs-lookup"><span data-stu-id="6c591-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="6c591-128">EREIGNIS</span><span class="sxs-lookup"><span data-stu-id="6c591-128">EVENT</span></span>                  | <span data-ttu-id="6c591-129">Das Steuerelement führt Anweisungen aus, die für das angegebene Ereignis definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6c591-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="6c591-130">Einfügen</span><span class="sxs-lookup"><span data-stu-id="6c591-130">FILENAME</span></span>               | <span data-ttu-id="6c591-131">Das-Steuerelement setzt seine **URL** -Eigenschaft zurück, versucht, die angegebene Datei zu öffnen, und beginnt sofort mit der Wiedergabe des neuen Streams.</span><span class="sxs-lookup"><span data-stu-id="6c591-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="6c591-132">OpenEvent</span><span class="sxs-lookup"><span data-stu-id="6c591-132">OPENEVENT</span></span>              | <span data-ttu-id="6c591-133">Puffert den zugeordneten Ereignistyp Befehl für die rechtzeitige Ausführung des Ereignis Skripts.</span><span class="sxs-lookup"><span data-stu-id="6c591-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="6c591-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="6c591-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="6c591-135">Der Parameter *param* enthält den synchronisierten Text.</span><span class="sxs-lookup"><span data-stu-id="6c591-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="6c591-136">In Windows Media Player wird der Text im Bereich geschlossene Überschrift der Funktion **jetzt abgespielt** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c591-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="6c591-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="6c591-137">TEXT</span></span>                   | <span data-ttu-id="6c591-138">Das-Steuerelement zeigt den zugeordneten Text im von iwmpclosedcaption angegebenen HTML-Element an. **captioningid**.</span><span class="sxs-lookup"><span data-stu-id="6c591-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="6c591-139">URL</span><span class="sxs-lookup"><span data-stu-id="6c591-139">URL</span></span>                    | <span data-ttu-id="6c591-140">Das-Steuerelement öffnet automatisch die URL, die mit dem Standard Internet Browser angegeben wird, wenn iwmpsettings. die **invokeurls** -Eigenschaft ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c591-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="6c591-141">Sie können beliebige andere Befehls Typen einbetten, solange Sie Code zum Verarbeiten des Befehls bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6c591-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="6c591-142">Obwohl unbekannte Befehle vom Windows Media Player-Steuerelement ignoriert werden, werden Sie weiterhin an das **ScriptCommand** -Ereignis übergeben.</span><span class="sxs-lookup"><span data-stu-id="6c591-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="6c591-143">Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei im schnell Forward-oder Rewind-Modus gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="6c591-144">URL-Befehle, die vom Windows-Media Player-Steuerelement empfangen werden, werden automatisch in Ihrem Standard Webbrowser aufgerufen, wenn iwmpsettings. die **invokeurls** -Eigenschaft ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6c591-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="6c591-145">Sie können die iwmpsettings verwenden. **defaultframe** -Eigenschaft, um den Zielframe anzugeben, in dem die Webseite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="6c591-146">Die an Windows Media Player gesendete URL wird relativ zur Basis-URL verarbeitet, die von iwmpsettings angegeben wird. **baseurl** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c591-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="6c591-147">Die Basis-URL wird mit dem relative URL verkettet, was zu einer vollständig angegebenen URL führt, die vom **ScriptCommand** -Ereignis als Befehlsparameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c591-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="6c591-148">Das Windows Media Player-Steuerelement verarbeitet eingehende URL-Befehle immer wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6c591-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="6c591-149">Ein URL-Type-Befehl wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="6c591-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="6c591-150">Iwmpsettings. **baseurl** wird verwendet, um eine vollständige URL aus der relative URL zu erstellen, die im Skript Befehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6c591-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="6c591-151">**ScriptCommand** wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c591-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="6c591-152">Nachdem **ScriptCommand** zurückgegeben wurde, iwmpsettings. **invokeurls** wird geprüft.</span><span class="sxs-lookup"><span data-stu-id="6c591-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="6c591-153">Wenn iwmpsettings. **invokeurls** ist true, und der Befehl ist ein URL-Befehl, die angegebene URL wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6c591-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="6c591-154">Wenn iwmpsettings. **invokeurls** ist false, oder wenn der Befehl kein URL-Befehl ist, wird der Befehl ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6c591-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="6c591-155">Wenn Sie eine Windows Media-Datei erstellen, können Sie angeben, in welchem Frame die neue URL angezeigt werden soll, indem Sie zwei kaufmännische und den Namen des Frames im Parameterfeld verketten.</span><span class="sxs-lookup"><span data-stu-id="6c591-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="6c591-156">Im folgenden Beispiel werden typische **ScriptCommand** -Parameter veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6c591-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="6c591-157">Er gibt an, dass die URL *MyPage* im Frame " *MyFrame* " gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="6c591-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="6c591-158">Das ScriptCommand-Ereignis wird nicht aufgerufen, wenn die Datei gescannt wird (schnell weitergeleitet oder reaktiviert).</span><span class="sxs-lookup"><span data-stu-id="6c591-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c591-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c591-159">Requirements</span></span>



| <span data-ttu-id="6c591-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c591-160">Requirement</span></span> | <span data-ttu-id="6c591-161">Wert</span><span class="sxs-lookup"><span data-stu-id="6c591-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c591-162">Version</span><span class="sxs-lookup"><span data-stu-id="6c591-162">Version</span></span><br/>   | <span data-ttu-id="6c591-163">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="6c591-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="6c591-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="6c591-164">Namespace</span></span><br/> | <span data-ttu-id="6c591-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="6c591-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="6c591-166">Assembly</span><span class="sxs-lookup"><span data-stu-id="6c591-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6c591-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6c591-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c591-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c591-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c591-169">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c591-170">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c591-171">**Iwmpclosedcaption. captioningid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c591-172">**Iwmpsettings. baseurl (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c591-173">**Iwmpsettings. defaultframe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6c591-174">**Iwmpsettings. invokeurls (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6c591-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





