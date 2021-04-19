---
title: Event-Element (WMP-SDK)
description: Das-Ereignis Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Windows Media Player-Ereignis Element
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370529"
---
# <a name="event-element"></a><span data-ttu-id="fae31-104">Event-Element</span><span class="sxs-lookup"><span data-stu-id="fae31-104">EVENT Element</span></span>

<span data-ttu-id="fae31-105">Das- **Ereignis** Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fae31-105">The **EVENT** element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span>

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a><span data-ttu-id="fae31-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="fae31-106">Attributes</span></span>

<span data-ttu-id="fae31-107">**Name** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="fae31-107">**NAME** (required)</span></span>

<span data-ttu-id="fae31-108">Der Name des Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="fae31-108">The name of the event.</span></span>

<span data-ttu-id="fae31-109">**Whendone** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="fae31-109">**WHENDONE** (required)</span></span>

<span data-ttu-id="fae31-110">Ein Wert, der definiert, welche Windows-Media Player nach dem Wiedergeben des referenzierten Inhalts funktioniert.</span><span class="sxs-lookup"><span data-stu-id="fae31-110">A value that defines what Windows Media Player does after playing the referenced content.</span></span>

<span data-ttu-id="fae31-111">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="fae31-111">The following values are possible.</span></span>



| <span data-ttu-id="fae31-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fae31-112">Value</span></span>  | <span data-ttu-id="fae31-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fae31-113">Description</span></span>                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae31-114">RESUME</span><span class="sxs-lookup"><span data-stu-id="fae31-114">RESUME</span></span> | <span data-ttu-id="fae31-115">Der aktuelle Eintrag (der durch das Ereignis unterbrochene Clip) setzt die Wiedergabe fort.</span><span class="sxs-lookup"><span data-stu-id="fae31-115">The current entry (the clip interrupted by the event) resumes playing.</span></span> <span data-ttu-id="fae31-116">Wenn der Inhalt als Inhalt gespeichert wird, wird er an derselben Stelle fortgesetzt, an der er angehalten wurde. Wenn der Inhalt übertragen wird, wird er an der aktuellen Position fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fae31-116">If the content is stored content, it resumes at the same point where it stopped; if the content is broadcast, it resumes at the current position.</span></span>        |
| <span data-ttu-id="fae31-117">NEXT</span><span class="sxs-lookup"><span data-stu-id="fae31-117">NEXT</span></span>   | <span data-ttu-id="fae31-118">Das nächste **Entry** -Element wird so abgespielt, als wäre das Ereignis nicht aufgetreten, und Windows Media Player hat das Ende des aktuellen Clips erreicht.</span><span class="sxs-lookup"><span data-stu-id="fae31-118">The next **ENTRY** element plays as if the event had not occurred and Windows Media Player had reached the end of the current clip.</span></span>                                                                                             |
| <span data-ttu-id="fae31-119">BREAK</span><span class="sxs-lookup"><span data-stu-id="fae31-119">BREAK</span></span>  | <span data-ttu-id="fae31-120">Wenn sich der aktuelle Eintrag innerhalb einer **Wiederholungs** Schleife befindet, wird die Schleife beendet, als ob die Wiederholungs Anzahl abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fae31-120">If the current entry is within a **REPEAT** loop, the loop terminates as if the repeat count had been completed.</span></span> <span data-ttu-id="fae31-121">Andernfalls springt Windows Media Player zum Ende der Wiedergabeliste, als wäre der abschließende Eintrag wie gewohnt abgeschlossen worden.</span><span class="sxs-lookup"><span data-stu-id="fae31-121">Otherwise, Windows Media Player jumps to the end of the playlist as if the final entry had completed as usual.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="fae31-122">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="fae31-122">Parent/Child Elements</span></span>



| <span data-ttu-id="fae31-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="fae31-123">Hierarchy</span></span>       | <span data-ttu-id="fae31-124">Elemente</span><span class="sxs-lookup"><span data-stu-id="fae31-124">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="fae31-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fae31-125">Parent elements</span></span> | <span data-ttu-id="fae31-126">**ASX**</span><span class="sxs-lookup"><span data-stu-id="fae31-126">**ASX**</span></span>                 |
| <span data-ttu-id="fae31-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fae31-127">Child elements</span></span>  | <span data-ttu-id="fae31-128">**Eintrag**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="fae31-128">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fae31-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fae31-129">Remarks</span></span>

<span data-ttu-id="fae31-130">Dieses Element definiert ein Verhalten oder eine Aktion, die von Windows Media Player ausgeführt wird, wenn ein Skript Befehl, der als Ereignis bezeichnet wird, empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="fae31-130">This element defines a behavior or action taken by Windows Media Player when it receives a script command labeled as an event.</span></span> <span data-ttu-id="fae31-131">Bei einem Ereignis handelt es sich um einen bestimmten Typ von Skript Befehl, der in einen an Windows gesendeten Stream eingebettet ist Media Player der aus einer doppelten Zeichenfolge besteht.</span><span class="sxs-lookup"><span data-stu-id="fae31-131">An event is a particular type of script command embedded in a stream sent to Windows Media Player that consists of a double string.</span></span> <span data-ttu-id="fae31-132">Die erste Zeichenfolge ist das Wort "Event", die zweite Zeichenfolge ist der Ereignis Name.</span><span class="sxs-lookup"><span data-stu-id="fae31-132">The first string is the word "event", and the second string is the event name.</span></span> <span data-ttu-id="fae31-133">Der Ereignis Name in der zweiten Zeichenfolge muss mit dem in der Metadatei definierten Ereignis Namen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="fae31-133">The event name in the second string must match the event name defined in the metafile.</span></span> <span data-ttu-id="fae31-134">(Bei der Entsprechung wird die Groß-/Kleinschreibung nicht beachtet. Ereignisse können an Windows gesendet werden, Media Player einen Echtzeit-Stream empfängt, oder Sie können in einer. ASF-, WMA-oder WMV-Datei gespeichert werden, die als Bedarfs gesteuerter unicaststream zugestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fae31-134">(The match is not case-sensitive.) Events can be sent to Windows Media Player receiving a real-time stream, or can be saved in an .asf, .wma, or .wmv file that gets delivered as an on-demand unicast stream.</span></span> <span data-ttu-id="fae31-135">Wenn Windows Media Player den Skript Befehl empfängt, wird das-Ereignis wie im- **Ereignis** Element definiert verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fae31-135">When Windows Media Player receives the script command, it processes the event as defined by the **EVENT** element.</span></span>

<span data-ttu-id="fae31-136">Dieses Element definiert einen Bereich von **Entry** -oder **ENTRYREF** -Elementen, die verarbeitet werden, wenn Windows Media Player den Skript Befehl mit dem benannten Ereignis empfängt.</span><span class="sxs-lookup"><span data-stu-id="fae31-136">This element defines a scope of **ENTRY** or **ENTRYREF** elements that are processed whenever Windows Media Player receives the script command with the named event.</span></span> <span data-ttu-id="fae31-137">**ENTRYREF** kann eine URL sein, die auf eine ASP-Seite verweist.</span><span class="sxs-lookup"><span data-stu-id="fae31-137">The **ENTRYREF** can be a URL that points to an ASP page.</span></span> <span data-ttu-id="fae31-138">Mit diesem Element können Sie ein Verhalten für den Datenstrom Wechsel nahezu in Echtzeit angeben, im Gegensatz zu vordefinierten streamänderungen, die Verweise auf andere Inhalts Teile oder Windows Media-Metadateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="fae31-138">With this element, you can specify a behavior for stream switching in near real time, as opposed to pre-authored stream changes using references to other pieces of content or Windows Media metafiles.</span></span>

<span data-ttu-id="fae31-139">Wenn Sie ASP-Seiten zum Generieren von Wiedergabelisten verwenden, müssen Sie einen Wert für die *Antwort* angeben. **ContentType** -Eigenschaft und die *Antwort*. **läuft** die Eigenschaft auf der ASP-Seite aufgrund von Latenzproblemen mit Windows-Media Player ab.</span><span class="sxs-lookup"><span data-stu-id="fae31-139">When you use ASP pages to generate playlists, you must specify a value for the *Response*.**ContentType** property and the *Response*.**expires** property in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="fae31-140">Die *Antwort*. **ContentType** muss eine gültige Dateinamenerweiterung für Windows Media-Metadateien sein.</span><span class="sxs-lookup"><span data-stu-id="fae31-140">The *Response*.**ContentType** must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="fae31-141">Gültige Typen sind:. ASF,. ASX,. WMA,. Wax,. WMV und. wvx.</span><span class="sxs-lookup"><span data-stu-id="fae31-141">Valid types include .asf, .asx, .wma, .wax, .wmv, and .wvx.</span></span>

<span data-ttu-id="fae31-142">Ausführliche Informationen zur Verwendung des **Antwort** Objekts in ASP finden Sie im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="fae31-142">See the Platform SDK for details about using the **Response** object in ASP.</span></span>

<span data-ttu-id="fae31-143">Dieses Element kann an beliebiger Stelle innerhalb des **ASX** -Elements vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fae31-143">This element can appear anywhere within the **ASX** element.</span></span> <span data-ttu-id="fae31-144">Wenn mehrere **Ereignis** Elemente in einem **ASX** -Element identische Werte für Ihre **namens** Attribute aufweisen, verwendet Windows Media Player das erste Vorkommen innerhalb des Elements " **ASX** " und ignoriert alle anderen Elemente.</span><span class="sxs-lookup"><span data-stu-id="fae31-144">If multiple **EVENT** elements within an **ASX** element have identical values for their **NAME** attributes, Windows Media Player uses the first occurrence within the **ASX** element, and ignores all others.</span></span> <span data-ttu-id="fae31-145">Wenn **Ereignis** Elemente über unterschiedliche **namens** Attribute verfügen, spielt die Reihen **Folge im-Element des-** Elements keine Rolle.</span><span class="sxs-lookup"><span data-stu-id="fae31-145">When **EVENT** elements have distinct **NAME** attributes, their order within the **ASX** element does not matter.</span></span>

<span data-ttu-id="fae31-146">Windows Media Player verwirft Ereignisse, die während der Verarbeitung eines anderen Ereignisses empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="fae31-146">Windows Media Player discards events it receives while processing another event.</span></span> <span data-ttu-id="fae31-147">Das Schachteln von Ereignissen wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fae31-147">Nesting of events is not supported.</span></span> <span data-ttu-id="fae31-148">Wenn sich Windows Media Player im Vorschaumodus befindet, wird der Ereignis Inhalt durch das **previewduration** -Element nicht eingeschränkt. die vollständige Länge der Ereignis Inhalte kann auch dann wiedergegeben werden, wenn die Vorschau Dauer für das aktive **Eintrags** Element vor dem Ende des Ereignisses abläuft.</span><span class="sxs-lookup"><span data-stu-id="fae31-148">When Windows Media Player is in preview mode, event content is not constrained by the **PREVIEWDURATION** element; the full length of event content can play even if the preview duration for the active **ENTRY** element expires prior to the end of the event.</span></span>

## <a name="examples"></a><span data-ttu-id="fae31-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fae31-149">Examples</span></span>

<span data-ttu-id="fae31-150">Wenn in diesem Beispiel Windows Media Player das Skript Befehls Ereignis und die Befehls Zeichenfolge "AdLINK" in den Streamingmedien empfängt, das Sie rendert, wird die Wiedergabeliste nach einem **EventName** "AdLINK" durchsucht.</span><span class="sxs-lookup"><span data-stu-id="fae31-150">In this example, when Windows Media Player receives the script command EVENT and command string "Adlink" in the streaming media it is rendering, it searches the playlist for an **EVENTNAME** "Adlink".</span></span> <span data-ttu-id="fae31-151">Windows Media Player schaltet von dem Stream, den er rendert, und gibt den Inhalt wieder, auf den im **Ereignis**"" verwiesen wird https://example.microsoft.com/adlink.htm .</span><span class="sxs-lookup"><span data-stu-id="fae31-151">Windows Media Player switches from the stream it is rendering and plays the content referenced in the **EVENT**, "https://example.microsoft.com/adlink.htm".</span></span>

<span data-ttu-id="fae31-152">Das **Eintrags** Attribut **clientskip** ist auf Nein festgelegt, um zu verhindern, dass der **Ereignis** Clip ausgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="fae31-152">**ENTRY** attribute **CLIENTSKIP** is set to NO to prevent the **EVENT** clip from being skipped.</span></span> <span data-ttu-id="fae31-153">Er muss wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fae31-153">It must be played.</span></span>

<span data-ttu-id="fae31-154">Das Skript `WHENDONE="RESUME"` weist Windows Media Player an, die Wiedergabe des vorherigen Mediums fortzusetzen, von dem es gewechselt hat, sobald "AdLINK. ASF" abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fae31-154">The script `WHENDONE="RESUME"` instructs Windows Media Player to resume playing the previous media it switched from as soon as Adlink.asf is finished.</span></span>


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="fae31-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fae31-155">Requirements</span></span>



| <span data-ttu-id="fae31-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fae31-156">Requirement</span></span> | <span data-ttu-id="fae31-157">Wert</span><span class="sxs-lookup"><span data-stu-id="fae31-157">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fae31-158">Version</span><span class="sxs-lookup"><span data-stu-id="fae31-158">Version</span></span><br/> | <span data-ttu-id="fae31-159">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fae31-159">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fae31-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fae31-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae31-161">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="fae31-161">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="fae31-162">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="fae31-162">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> <dt>

[<span data-ttu-id="fae31-163">**Windows Media Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="fae31-163">**Windows Media Player Object Model**</span></span>](windows-media-player-object-model.md)
</dt> </dl>

 

 





