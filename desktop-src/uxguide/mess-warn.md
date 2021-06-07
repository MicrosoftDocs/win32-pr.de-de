---
title: Warnmeldungen
description: Eine Warnmeldung ist ein modales Dialogfeld, eine ortsbezogene Nachricht, eine Benachrichtigung oder eine Sprechblase, mit der der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft zu einem Problem führen kann.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 42f7c669a68790ec290f931165b4aa937b5008d5
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524504"
---
# <a name="warning-messages"></a><span data-ttu-id="0f7f2-103">Warnmeldungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="0f7f2-104">Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="0f7f2-105">Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="0f7f2-106">Eine Warnmeldung ist ein modales Dialogfeld, eine ortsbezogene Nachricht, eine Benachrichtigung oder eine Sprechblase, mit der der Benutzer über eine Bedingung benachrichtigt wird, die in Zukunft zu einem Problem führen kann.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![Screenshot einer typischen Warnmeldung](images/mess-warn-image1.png)

<span data-ttu-id="0f7f2-108">Eine typische modale Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-108">A typical modal warning message.</span></span>

<span data-ttu-id="0f7f2-109">Das grundlegende Merkmal von Warnungen besteht darin, dass sie das Risiko mit sich bringen, einen oder mehrere der folgenden Punkte zu verlieren:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="0f7f2-110">Eine wertvolle Ressource, z. B. wichtige Finanzdaten oder andere Daten.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="0f7f2-111">Systemzugriff oder -integrität.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-111">System access or integrity.</span></span>
-   <span data-ttu-id="0f7f2-112">Datenschutz oder Kontrolle über vertrauliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="0f7f2-113">Die Zeit des Benutzers (eine erhebliche Menge, z. B. 30 Sekunden oder mehr).</span><span class="sxs-lookup"><span data-stu-id="0f7f2-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="0f7f2-114">Im Gegensatz dazu ist eine Bestätigung ein modales Dialogfeld, in dem gefragt wird, ob der Benutzer mit einer Aktion fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="0f7f2-115">Einige Arten von Warnungen werden als Bestätigungen angezeigt, und wenn ja, gelten auch die Bestätigungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="0f7f2-116">**Hinweis:** Richtlinien im Zusammenhang mit [Dialogfeldern,](win-dialog-box.md) [Bestätigungen,](mess-confirm.md) [Fehlermeldungen](mess-error.md)[Standardsymbole,](vis-std-icons.md) [Benachrichtigungen](mess-notif.md)und [Layout](vis-layout.md) werden in separaten Artikeln dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="0f7f2-117">Ist dies die richtige Benutzeroberfläche?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-117">Is this the right user interface?</span></span>

<span data-ttu-id="0f7f2-118">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="0f7f2-119">**Wird der Benutzer über eine Bedingung benachrichtigt, die in Zukunft ein Problem verursachen kann?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="0f7f2-120">Wenn nicht, ist die Nachricht keine Warnung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="0f7f2-121">**Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das bereits aufgetreten ist?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="0f7f2-122">Verwenden Sie in diesem Falle stattdessen eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="0f7f2-123">**Führen Benutzer wahrscheinlich eine Aktion aus oder ändern ihr Verhalten als Ergebnis der Nachricht?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="0f7f2-124">Wenn dies nicht der Lage ist, kann der Benutzer durch die Bedingung nicht unterbrochen werden. Daher ist es besser, die Warnung zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="0f7f2-125">**Ist die Bedingung das direkte Ergebnis einer vom Benutzer initiierten Aktion?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="0f7f2-126">Wenn dies nicht der Fall ist, sollten Sie eine [nicht kritische Ereignisbenachrichtigung](mess-notif.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="0f7f2-127">**Ist die Bedingung eine besondere Bedingung in einem Steuerelement?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="0f7f2-128">Verwenden Sie in diesem Falle stattdessen einen [Balloon.](ctrl-balloons.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="0f7f2-129">**Ist der Benutzer bereit, eine riskante Aktion auszuführen, um Bestätigungen zu erhalten?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="0f7f2-130">In diesem Falle ist eine Warnung geeignet, wenn die Aktion erhebliche Konsequenzen hat oder nicht einfach rückgängig zu werden ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="0f7f2-131">**Muss der Benutzer für andere Arten von Warnungen jetzt oder in der unmittelbaren Zukunft handeln?**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="0f7f2-132">Zeigen Sie keine Warnungen an, wenn Benutzer weiterhin ohne sofortige Probleme produktiv arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="0f7f2-133">Verschieben Sie die Warnung, bis die Bedingung direkter und relevanter ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="0f7f2-134">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="0f7f2-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="0f7f2-135">Vermeiden von Überwarnungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-135">Avoid overwarning</span></span>

<span data-ttu-id="0f7f2-136">Wir haben in Microsoft Windows-Programmen überwarnt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="0f7f2-137">Das typische Windows-Programm verfügt scheinbar überall über Warnungen, warnungen zu Dingen, die nur eine geringe Bedeutung haben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="0f7f2-138">In einigen Programmen wird fast jede Frage als Warnung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="0f7f2-139">Eine Überhärtung bewirkt, dass die Verwendung eines Programms sich wie eine gefährliche Aktivität anfühlt und von wirklich signifikanten Problemen abweicht.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="0f7f2-140">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-140">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-141">Screenshot einer unnötigen Warnmeldung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="0f7f2-142">Überwarnungen machen Ihr Programm gefährlich und sehen so aus, als ob es von Dern entwickelt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="0f7f2-143">Das reine Potenzial für Datenverlust oder ein zukünftiges Problem allein reicht nicht aus, um eine Warnung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="0f7f2-144">Darüber hinaus sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt sein und nicht einfach korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="0f7f2-145">Andernfalls kann fast jeder Benutzerfehler behoben werden, um zu Datenverlust oder einem potenziellen Problem einer Art zu führen und eine Warnung auszulösen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="0f7f2-146">Merkmale guter Warnungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-146">Characteristics of good warnings</span></span>

<span data-ttu-id="0f7f2-147">Gute Warnungen:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-147">Good warnings:</span></span>

-   <span data-ttu-id="0f7f2-148">**Risiko einbeziehen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-148">**Involve risk.**</span></span> <span data-ttu-id="0f7f2-149">Gute Warnungen warnen Benutzer vor etwas, das von Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="0f7f2-150">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-150">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-151">Screenshot von "Möchten Sie beenden?"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="0f7f2-152">warning</span><span class="sxs-lookup"><span data-stu-id="0f7f2-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="0f7f2-153">Na und?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-153">So what?</span></span> <span data-ttu-id="0f7f2-154">Bei dieser Bestätigung wird davon ausgegangen, dass Benutzer Programme häufig aus Versehen beenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="0f7f2-155">**Unmittelbar relevant.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-155">**Have immediate relevance.**</span></span> <span data-ttu-id="0f7f2-156">Benutzer müssen sich nicht nur darum kümmern, sie müssen sich jetzt darum kümmern.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="0f7f2-157">Benutzer sind in der Regel nicht an Problemen interessiert, die sie möglicherweise später haben, solange sie ihre Arbeit jetzt erledigen können.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="0f7f2-158">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-158">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-159">Screenshot der Warnung "Battery-low-in-three-hours"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="0f7f2-160">In diesem Fall ist es besser, den Benutzer in drei Stunden zu warnen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="0f7f2-161">**Führen Sie zu einer Aktion.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-161">**Lead to action.**</span></span> <span data-ttu-id="0f7f2-162">Es gibt etwas, das Benutzer als Ergebnis der Warnung tun oder beachten müssen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="0f7f2-163">Möglicherweise müssen sie jetzt oder in der unmittelbaren Zukunft eine Aktion ergreifen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="0f7f2-164">Möglicherweise führen sie daher eine Aufgabe anders aus.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="0f7f2-165">Die Folge des Ignorierens der Warnung sollte klar sein.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="0f7f2-166">Warnungen ohne Aktionen sorgen nur dafür, dass Benutzer paranoid sind.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="0f7f2-167">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-167">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-168">Screenshot der Warnung "Live Messenger wird ausgeführt"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="0f7f2-169">Warum ist diese Benachrichtigung eine Warnung?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-169">Why is this notification a warning?</span></span> <span data-ttu-id="0f7f2-170">Was sollen Benutzer tun (neben der Sorge)?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="0f7f2-171">**Dies ist nicht offensichtlich.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-171">**Are not obvious.**</span></span> <span data-ttu-id="0f7f2-172">Zeigen Sie keine Warnung an, um die offensichtliche Folge einer Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="0f7f2-173">Nehmen Sie beispielsweise an, dass Benutzer die Konsequenzen verstehen, die sich ergeben, wenn eine Aufgabe nicht abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="0f7f2-174">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-174">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-175">Screenshot: Möchten Sie den Assistenten beenden? Warnung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="0f7f2-176">Das Abbrechen eines unvollständigen Assistenten bedeutet, dass die Aufgabe nicht abgeschlossen wird... wer wusste?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="0f7f2-177">**Tritt selten auf.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-177">**Occur infrequently.**</span></span> <span data-ttu-id="0f7f2-178">Konstante Warnungen werden schnell ineffektiv und ungern.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="0f7f2-179">Benutzer konzentrieren sich häufig eher darauf, die Warnung zu entfernen, als das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="0f7f2-180">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-180">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-181">Screenshot der Warnung "Virussignaturen aktualisieren"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="0f7f2-182">Benutzer konzentrieren sich eher darauf, die Warnung zu entfernen, als das zugrunde liegende Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="0f7f2-183">Eine Nachricht, die diese Merkmale nicht aufweist, ist möglicherweise dennoch eine gute Nachricht, keine gute Warnung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="0f7f2-184">Bestimmen des geeigneten Nachrichtentyps</span><span class="sxs-lookup"><span data-stu-id="0f7f2-184">Determine the appropriate message type</span></span>

<span data-ttu-id="0f7f2-185">Einige Probleme können je nach Schwerpunkt und Ausdruck als Fehler, Warnung oder Information dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="0f7f2-186">Angenommen, eine Webseite kann basierend auf der aktuellen Windows Internet Explorer-Konfiguration kein nicht signiertes ActiveX-Steuerelement laden:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="0f7f2-187">**Fehler.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-187">**Error.**</span></span> <span data-ttu-id="0f7f2-188">"Diese Seite kann kein ActiveX-Steuerelement ohne Vorzeichen laden."</span><span class="sxs-lookup"><span data-stu-id="0f7f2-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="0f7f2-189">(Wird als vorhandenes Problem bezeichnet.)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="0f7f2-190">**Warnung.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-190">**Warning.**</span></span> <span data-ttu-id="0f7f2-191">"Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von ActiveX-Steuerelementen ohne Vorzeichen konfiguriert ist."</span><span class="sxs-lookup"><span data-stu-id="0f7f2-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="0f7f2-192">oder "Zulassen, dass diese Seite ein nicht signiertes ActiveX-Steuerelement installiert?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="0f7f2-193">Wenn Sie dies aus nicht vertrauenswürdigen Quellen tun, kann dies ihrem Computer schaden."</span><span class="sxs-lookup"><span data-stu-id="0f7f2-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="0f7f2-194">(Beide werden als Bedingungen bezeichnet, die zukünftige Probleme verursachen können.)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="0f7f2-195">**Informationen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-195">**Information.**</span></span> <span data-ttu-id="0f7f2-196">"Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden."</span><span class="sxs-lookup"><span data-stu-id="0f7f2-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="0f7f2-197">(Als Faktenhinweis formuliert.)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="0f7f2-198">**Um den geeigneten Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, den Benutzer kennen oder reagieren müssen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="0f7f2-199">Wenn ein Problem den Benutzer daran hindert, fortzufahren, sollten Sie ihn in der Regel als Fehler darstellen. Wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung dar.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="0f7f2-200">Erstellen Sie die [Hauptanweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol[(Standard](vis-std-icons.md) oder anderweitig) aus, das dem Text entspricht.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="0f7f2-201">Der Hauptanweisungstext und die Symbole sollten immer übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="0f7f2-202">Spezifisch sein</span><span class="sxs-lookup"><span data-stu-id="0f7f2-202">Be specific</span></span>

<span data-ttu-id="0f7f2-203">Warnungen sind überzeugender, wenn die folgenden Informationen spezifisch und eindeutig sind:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="0f7f2-204">Die Quelle der Warnung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-204">The source of the warning.</span></span>
-   <span data-ttu-id="0f7f2-205">Die spezifische Bedingung und das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="0f7f2-206">Was der Benutzer tun sollte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-206">What the user should do about it.</span></span>
-   <span data-ttu-id="0f7f2-207">Was geschieht, wenn der Benutzer nichts tut?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="0f7f2-208">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-208">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-209">Screenshot: Warnung vor erheblichem Risiko</span><span class="sxs-lookup"><span data-stu-id="0f7f2-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="0f7f2-210">Was ist das potenzielle Problem in diesem Beispiel?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="0f7f2-211">Was soll der Benutzer tun, abgesehen davon, dass der Projektor nicht über das Netzwerk verwendet wird?</span><span class="sxs-lookup"><span data-stu-id="0f7f2-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="0f7f2-212">Ohne spezifischere Informationen kann der Benutzer nicht fortfahren.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="0f7f2-213">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-213">**Correct:**</span></span>

![<span data-ttu-id="0f7f2-214">Screenshot: Warnung vor Problem und Folgen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="0f7f2-215">In diesem Beispiel sind das Problem und die Konsequenzen klar.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="0f7f2-216">Manchmal besteht ein legitimes potenzielles Problem, benutzer zu informieren, aber die Lösung und die Konsequenzen sind nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="0f7f2-217">Anstatt eine ungenaue Warnung zu geben, sollten Sie spezifisch sein, indem Sie die wahrscheinlichsten Informationen oder das gängigste Beispiel geben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="0f7f2-218">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-218">**Correct:**</span></span>

![<span data-ttu-id="0f7f2-219">Screenshot: Netzwerkfehlerwarnung und Lösungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="0f7f2-220">In diesem Beispiel wird die Warnung spezifisch gemacht, indem die wahrscheinlichste Lösung zur Verfügung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="0f7f2-221">Verwenden Sie in solchen Fällen jedoch Formulierungen, die darauf hindeutet, dass es andere Möglichkeiten gibt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="0f7f2-222">Andernfalls kann es sein, dass Benutzer verfehlt werden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="0f7f2-223">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-223">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-224">Screenshot der Netzwerkkabel-Entkabelungswarnung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="0f7f2-225">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-225">**Correct:**</span></span>

![<span data-ttu-id="0f7f2-226">Screenshot des Kabels ist möglicherweise nicht angeschlossen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="0f7f2-227">Im falschen Beispiel sind Benutzer verwirrend, wenn das Kabel eindeutig angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="0f7f2-228">**Wenn Sie nur zwei Dinge tun...**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="0f7f2-229">Nicht überwarnen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-229">Don't overwarn.</span></span> <span data-ttu-id="0f7f2-230">Beschränken Sie Warnungen auf Bedingungen, die risikenind und sofort relevant, umsetzbar, nicht offensichtlich und selten sind.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="0f7f2-231">Entfernen oder umformulieren Sie andernfalls die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="0f7f2-232">Geben Sie spezifische, nützliche Informationen an.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="0f7f2-233">Verwendungsmuster</span><span class="sxs-lookup"><span data-stu-id="0f7f2-233">Usage patterns</span></span>

<span data-ttu-id="0f7f2-234">Warnungen haben mehrere Verwendungsmuster:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f7f2-235"><strong>Bewusstsein</strong></span><span class="sxs-lookup"><span data-stu-id="0f7f2-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="0f7f2-236">Machen Sie den Benutzer auf eine Bedingung oder ein potenzielles Problem aufmerksam, aber der Benutzer muss jetzt möglicherweise nichts tun.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="0f7f2-237">Beispiele für Warnungen zu Bewusstsein.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="0f7f2-238">Warnungen zu Bewusstseinswarnungen haben die folgende Darstellung:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="0f7f2-239"><strong>Hauptanweisung:</strong> Beschreiben Sie die Bedingung oder das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="0f7f2-240"><strong>Zusätzliche Anweisung:</strong> Erläutern Sie die Implikation und warum sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="0f7f2-241"><strong>Commitschaltflächen:</strong> Schließen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f7f2-242"><strong>Fehlerschutz</strong></span><span class="sxs-lookup"><span data-stu-id="0f7f2-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="0f7f2-243">Machen Sie den Benutzer auf Informationen aufmerksam, die ein Problem verhindern können, insbesondere wenn Sie Entscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="0f7f2-244">Fehlerschutzwarnungen werden am besten mit einem symbol für eine warnungsbasierte Warnung und einem erläuternden Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="0f7f2-245">Beispiele für Fehlerschutzwarnungen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f7f2-246"><strong>Bevorstehendes Problem</strong></span><span class="sxs-lookup"><span data-stu-id="0f7f2-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="0f7f2-247">Der Benutzer muss jetzt etwas tun, um ein bevorstehendes Problem zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="0f7f2-248">Ein Beispiel für eine Warnung zu einem bevorstehenden Problem.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="0f7f2-249">Warnungen zu einem bevorstehenden Problem haben die folgende Darstellung:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="0f7f2-250"><strong>Hauptanweisung:</strong> Beschreiben Sie, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="0f7f2-251"><strong>Zusätzliche Anweisung:</strong> Erläutern Sie die Bedingung und deren Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="0f7f2-252"><strong>Commitschaltflächen:</strong> Eine Befehlsschaltfläche oder ein Befehlslink für jede Option oder OK, wenn die Aktion außerhalb des Dialogfelds erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f7f2-253"><strong>Bestätigung riskanter Aktionen</strong></span><span class="sxs-lookup"><span data-stu-id="0f7f2-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="0f7f2-254">Vergewissern Sie sich, dass der Benutzer mit einer Aktion fortfahren möchte, die ein gewisses Risiko auf sich hat und nicht einfach rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="0f7f2-255">Ein Beispiel für die Bestätigung riskanter Aktionen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="0f7f2-256">Bestätigungen für riskante Aktionen haben die folgende Darstellung:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="0f7f2-257"><strong>Hauptanweisung:</strong> Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="0f7f2-258"><strong>Zusätzliche Anweisung:</strong> Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="0f7f2-259"><strong>Commitschaltflächen:</strong> Ja, Nein.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="0f7f2-260">Richtlinien zu diesem Muster finden Sie unter <a href="mess-confirm.md">Bestätigungen.</a></span><span class="sxs-lookup"><span data-stu-id="0f7f2-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="0f7f2-261">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0f7f2-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="0f7f2-262">Präsentation</span><span class="sxs-lookup"><span data-stu-id="0f7f2-262">Presentation</span></span>

-   <span data-ttu-id="0f7f2-263">**Wählen Sie die Präsentationsbenutzeroberfläche basierend auf dem Informationstyp aus:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-263">**Choose the presentation UI based on the type of information:**</span></span>



| <span data-ttu-id="0f7f2-264">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="0f7f2-264">User interface</span></span>  | <span data-ttu-id="0f7f2-265">Am besten verwendet für</span><span class="sxs-lookup"><span data-stu-id="0f7f2-265">Best used for</span></span> |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7f2-266">Modale Dialogfelder</span><span class="sxs-lookup"><span data-stu-id="0f7f2-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="0f7f2-267">Kritische Warnungen (einschließlich Bestätigungen), auf die Benutzer jetzt reagieren müssen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="0f7f2-268">In-Place</span><span class="sxs-lookup"><span data-stu-id="0f7f2-268">In-place</span></span><br/>           | <span data-ttu-id="0f7f2-269">Informationen, die ein Problem verhindern können, insbesondere, wenn Benutzer Entscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="0f7f2-270">Banner</span><span class="sxs-lookup"><span data-stu-id="0f7f2-270">Banners</span></span><br/>            | <span data-ttu-id="0f7f2-271">Informationen, die ein Problem verhindern können, insbesondere im Zusammenhang mit dem Abschließen einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="0f7f2-272">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-272">Notifications</span></span><br/>      | <span data-ttu-id="0f7f2-273">Wichtige Ereignisse oder Status, die zumindest vorübergehend ignoriert werden können.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="0f7f2-274">Ballons</span><span class="sxs-lookup"><span data-stu-id="0f7f2-274">Balloons</span></span><br/>           | <span data-ttu-id="0f7f2-275">Ein Steuerelement befindet sich in einem Zustand, der die Eingabe beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-275">A control is in a state that affects input.</span></span> <span data-ttu-id="0f7f2-276">Dieser Zustand ist wahrscheinlich unbeabsichtigt, und der Benutzer erkennt möglicherweise nicht, dass die Eingabe betroffen ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="0f7f2-277">**Für modale Dialogfelder:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="0f7f2-278">**Verwenden Sie Taskdialoge, wenn dies angemessen ist, um ein konsistentes Aussehen und Layout zu erzielen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="0f7f2-279">Taskdialogfelder erfordern Windows Vista oder höher, sodass sie nicht für frühere Versionen von Windows geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="0f7f2-280">**Zeigt nur eine Warnmeldung pro Bedingung an.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="0f7f2-281">Zeigen Sie z. B. eine einzelne Warnung an, die eine Bedingung vollständig erklärt, anstatt sie nach und nach pro Nachricht zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="0f7f2-282">Das Anzeigen einer Sequenz von Warndialogfeldern für eine einzelne Bedingung ist verwirrend und verwirrend.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="0f7f2-283">**Zeigen Sie eine Warnung nicht mehr als einmal pro Bedingung an.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="0f7f2-284">Konstante Warnungen werden schnell ineffektiv und lästig.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="0f7f2-285">Benutzer konzentrieren sich häufig eher darauf, die Warnung zu beheben, als das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="0f7f2-286">Wenn Sie wiederholt bei einer einzelnen Bedingung warnen müssen, verwenden Sie [progressive Eskalation.](mess-notif.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="0f7f2-287">**Warnungen werden nicht mit einem Soundeffekt oder Signalton begleitet.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="0f7f2-288">Dies ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="0f7f2-289">**Ausnahme:** Wenn der Benutzer sofort reagieren muss, können Sie einen Soundeffekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="0f7f2-290">Symbole</span><span class="sxs-lookup"><span data-stu-id="0f7f2-290">Icons</span></span>

-   <span data-ttu-id="0f7f2-291">Platzieren Sie in der Titelleiste eines Dialogfelds kein Warnsymbol.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="0f7f2-292">**Verwenden Sie ein Warnsymbol.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-292">**Use a warning icon.**</span></span> <span data-ttu-id="0f7f2-293">Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-293">Exceptions:</span></span>
    -   <span data-ttu-id="0f7f2-294">Wenn die Warnung für ein Feature mit einem Symbol gilt, können Sie das Featuresymbol mit einer Warnüberlagerung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="0f7f2-295">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-295">**Correct:**</span></span>

        ![<span data-ttu-id="0f7f2-296">Screenshot des Sperrsymbols mit Überlagerung des Warnsymbols</span><span class="sxs-lookup"><span data-stu-id="0f7f2-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="0f7f2-297">In diesem Beispiel verfügt das Featuresymbol über eine Warnüberlagerung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="0f7f2-298">Legen Sie für modale Dialogfelder mit einer Fußnote mit Einer Warnung das Warnsymbol in die Fußnote und nicht in den Inhaltsbereich.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="0f7f2-299">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-299">**Correct:**</span></span>

    ![<span data-ttu-id="0f7f2-300">Screenshot des Warnsymbols in der Fußnote des Dialogfelds</span><span class="sxs-lookup"><span data-stu-id="0f7f2-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="0f7f2-301">In diesem Beispiel weist die Fußnote das Warnsymbol auf.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="0f7f2-302">Weitere Richtlinien und Beispiele finden Sie unter [Standardsymbole.](vis-std-icons.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="0f7f2-303">Diese Meldung nicht erneut anzeigen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-303">Don't show this message again</span></span>

-   <span data-ttu-id="0f7f2-304">**Wenn diese Option für ein Warnungsdialogfeld erforderlich ist, sollten Sie die Warnung und ihre Häufigkeit überprüfen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="0f7f2-305">Wenn sie alle Merkmale einer guten Warnung aufweist (risikobezieht und sofort relevant, umsetzbar, nicht offensichtlich und selten ist), sollte es für Benutzer nicht sinnvoll sein, sie zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="0f7f2-306">Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f2-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="0f7f2-307">Schrittweise Offenlegung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-307">Progressive disclosure</span></span>

-   <span data-ttu-id="0f7f2-308">**Wenn Sie erweiterte Informationen in eine Warnmeldung einschließen müssen, können Sie sie mithilfe von Schaltflächen** für die progressive Offenlegung anzeigen (z. B. "Details anzeigen").</span><span class="sxs-lookup"><span data-stu-id="0f7f2-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="0f7f2-309">Dadurch wird die Warnung für die typische Verwendung vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="0f7f2-310">Blenden Sie die benötigten Informationen nicht aus, da benutzer sie möglicherweise nicht finden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="0f7f2-311">**Verwenden Sie nicht "Details anzeigen", es sei denn, es gibt wirklich mehr Details.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="0f7f2-312">Stellen Sie nicht einfach die vorhandenen Informationen in einem anderen Format wieder her.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="0f7f2-313">Informationen zu Bezeichnungsrichtlinien finden Sie unter [Progressive Offenlegung.](ctrl-progressive-disclosure-controls.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="0f7f2-314">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="0f7f2-314">Default values</span></span>

-   <span data-ttu-id="0f7f2-315">**Wählen Sie die sicherste, am wenigsten destruktive oder sicherste Antwort als Standard aus.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="0f7f2-316">Text</span><span class="sxs-lookup"><span data-stu-id="0f7f2-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="0f7f2-317">Allgemein</span><span class="sxs-lookup"><span data-stu-id="0f7f2-317">General</span></span>

-   <span data-ttu-id="0f7f2-318">**Entfernen Sie redundanten Text.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-318">**Remove redundant text.**</span></span> <span data-ttu-id="0f7f2-319">Suchen Sie in Titeln, Hauptanweisungen, zusätzlichen Anweisungen, Inhaltsbereich, Befehlslinks und Commitschaltflächen danach.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="0f7f2-320">Lassen Sie im Allgemeinen vollständigen Text in Anweisungen und interaktiven Steuerelementen, und entfernen Sie redundanzen von den anderen Stellen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="0f7f2-321">**Verwenden Sie nicht die Begriffe "Warnung" oder "Vorsicht" im Text.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="0f7f2-322">Bei [ordnungsgemäßer Verwendung](vis-std-icons.md)kommuniziert das Warnsymbol ausreichend, dass Benutzer mit Vorsicht vorgehen müssen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="0f7f2-323">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-323">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-324">Screenshot der unnötigen Verwendung von Warnungen im Text</span><span class="sxs-lookup"><span data-stu-id="0f7f2-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="0f7f2-325">In diesem Beispiel ist der Begriff "Warnung" nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="0f7f2-326">Titel</span><span class="sxs-lookup"><span data-stu-id="0f7f2-326">Titles</span></span>

-   <span data-ttu-id="0f7f2-327">**Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Warnung stammt.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="0f7f2-328">Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-328">Exceptions:</span></span>
    -   <span data-ttu-id="0f7f2-329">Wenn eine Warnung von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="0f7f2-330">Wenn dieser Titel redundant oder verwirrend mit der Hauptanweisung wäre, verwenden Sie stattdessen den Programmnamen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="0f7f2-331">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-331">**Incorrect:**</span></span>

![<span data-ttu-id="0f7f2-332">Screenshot des Titels des Dialogfelds "Sicherheitswarnung"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="0f7f2-333">In diesem Beispiel identifiziert "Sicherheitswarnung" nicht den Befehl oder das Feature, von dem die Warnung stammt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="0f7f2-334">**Verwenden Sie den Titel nicht, um zu erläutern, was im Dialogfeld ausgeführt** werden soll, das der Zweck der Hauptanweisung ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="0f7f2-335">Verwenden Sie [die Groß-/Großschreibung im Titelformat,](glossary.md)ohne die Interpunktion zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="0f7f2-336">Hauptanweisungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-336">Main instructions</span></span>

-   <span data-ttu-id="0f7f2-337">Die Hauptanweisung für eine Warnung basiert auf ihrem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-337">The main instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="0f7f2-338">Muster</span><span class="sxs-lookup"><span data-stu-id="0f7f2-338">Pattern</span></span>                        | <span data-ttu-id="0f7f2-339">Hauptanweisung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-339">Main instruction</span></span>                                               |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="0f7f2-340">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="0f7f2-340">Awareness</span></span><br/>                 | <span data-ttu-id="0f7f2-341">Beschreiben Sie die Bedingung oder das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="0f7f2-342">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="0f7f2-342">Imminent problem</span></span><br/>          | <span data-ttu-id="0f7f2-343">Beschreiben Sie, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="0f7f2-344">Bestätigung riskanter Aktionen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="0f7f2-345">Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="0f7f2-346">Screenshot einer Benachrichtigung mit geringem Akkustand</span><span class="sxs-lookup"><span data-stu-id="0f7f2-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="0f7f2-347">In diesem Beispiel ist die Benachrichtigung über niedrige Akkukapazität eine Warnung zur Benachrichtigung des Bewusstseins, sodass die Hauptanweisung die Bedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="0f7f2-348">Screenshot der Warnung zum sofortigen Wechsel des Akkus</span><span class="sxs-lookup"><span data-stu-id="0f7f2-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="0f7f2-349">In diesem Beispiel ist das Dialogfeld mit geringem Akkustand ein bevorstehendes Problem. Daher wird in der Hauptanweisung beschrieben, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="0f7f2-350">**Verwenden Sie nur einen einzigen vollständigen Satz.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="0f7f2-351">Legen Sie die Hauptanweisung auf die wesentlichen Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="0f7f2-352">Wenn Sie weitere Informationen benötigen, verwenden Sie eine ergänzende Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="0f7f2-353">**Verwenden Sie Wörter wie "jetzt" und "sofort", wenn der Benutzer sofort handeln muss.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="0f7f2-354">Verwenden Sie diese Wörter nicht, wenn es keine Dringendkeit gibt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="0f7f2-355">**Geben Sie den vollständigen Namen an, wenn Objekte beteiligt sind.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="0f7f2-356">Verwenden Sie [die Groß-/Großschreibung im Satzformat.](glossary.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f2-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="0f7f2-357">Zusätzliche Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-357">Supplemental instructions</span></span>

-   <span data-ttu-id="0f7f2-358">Die ergänzende Anweisung für eine Warnung basiert auf ihrem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



| <span data-ttu-id="0f7f2-359">Muster</span><span class="sxs-lookup"><span data-stu-id="0f7f2-359">Pattern</span></span>            | <span data-ttu-id="0f7f2-360">Ergänzende Anweisung</span><span class="sxs-lookup"><span data-stu-id="0f7f2-360">Supplemental instruction</span></span>                                            |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7f2-361">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="0f7f2-361">Awareness</span></span><br/>                 | <span data-ttu-id="0f7f2-362">Erläutern Sie die Auswirkungen und warum dies wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="0f7f2-363">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="0f7f2-363">Imminent problem</span></span><br/>          | <span data-ttu-id="0f7f2-364">Erläutern Sie die Bedingung und warum sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="0f7f2-365">Bestätigung riskanter Aktionen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="0f7f2-366">Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="0f7f2-367">**Wiederholen Sie die Hauptanweisung nicht mit leicht abweichenden Formulierungen.**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="0f7f2-368">Lassen Sie stattdessen die zusätzliche Anweisung aus, wenn nicht mehr hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="0f7f2-369">Verwenden Sie vollständige Sätze, Groß- und Großschreibung im Satzstil und endende Interpunktion.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="0f7f2-370">Commitschaltflächen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-370">Commit buttons</span></span>

-   <span data-ttu-id="0f7f2-371">Für Warndialogfelder basieren die Commitschaltflächen auf ihrem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



| <span data-ttu-id="0f7f2-372">Muster</span><span class="sxs-lookup"><span data-stu-id="0f7f2-372">Pattern</span></span>               | <span data-ttu-id="0f7f2-373">Commitschaltflächen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-373">Commit buttons</span></span>        |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7f2-374">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="0f7f2-374">Awareness</span></span><br/>                 | <span data-ttu-id="0f7f2-375">Fast richtig.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-375">Close.</span></span> <span data-ttu-id="0f7f2-376">Verwenden Sie ok nicht, da dies darauf hindeutet, dass potenzielle Probleme in Ordnung sind.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="0f7f2-377">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="0f7f2-377">Imminent problem</span></span><br/>          | <span data-ttu-id="0f7f2-378">Eine Befehlsschaltfläche oder ein Befehlslink für jede Option oder OK, wenn die Aktion außerhalb des Dialogfelds auftritt.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="0f7f2-379">Bestätigung riskanter Aktionen</span><span class="sxs-lookup"><span data-stu-id="0f7f2-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="0f7f2-380">Ja, Nein.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="0f7f2-381">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="0f7f2-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="0f7f2-382">Screenshot des Dialogfelds "Warnung" mit schaltfläche "OK"</span><span class="sxs-lookup"><span data-stu-id="0f7f2-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="0f7f2-383">Probleme sind nicht in Ordnung, verwenden Sie stattdessen Schließen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="0f7f2-384">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="0f7f2-384">Documentation</span></span>

<span data-ttu-id="0f7f2-385">Beim Verweisen auf Warnungen:</span><span class="sxs-lookup"><span data-stu-id="0f7f2-385">When referring to warnings:</span></span>

-   <span data-ttu-id="0f7f2-386">Wenn die Warnung eine Frage stellt, verweisen Sie anhand ihrer Frage auf eine Warnung. Verwenden Sie andernfalls die Main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="0f7f2-387">Wenn die Frage oder die Hauptanweisung lang oder ausführlich ist, fassen Sie sie zusammen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="0f7f2-388">Bei Bedarf können Sie auf ein Warndialogfeld als Meldung verweisen.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="0f7f2-389">Formatieren Sie den Text nach Möglichkeit fett.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-389">When possible, format the text using bold.</span></span> <span data-ttu-id="0f7f2-390">Andernfalls setzen Sie den Text nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="0f7f2-391">Beispiel: Klicken Sie in der Meldung **Möchten Sie die unsicheren Elemente anzeigen?** auf Ja.</span><span class="sxs-lookup"><span data-stu-id="0f7f2-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

