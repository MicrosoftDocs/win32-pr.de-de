---
title: Warnmeldungen
description: Eine Warnmeldung ist ein modales Dialogfeld, eine direkte Nachricht, eine Benachrichtigung oder eine Sprechblase, die den Benutzer über eine Bedingung benachrichtigt, die möglicherweise in der Zukunft ein Problem verursacht.
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351088"
---
# <a name="warning-messages"></a><span data-ttu-id="f5b4b-103">Warnmeldungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="f5b4b-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f5b4b-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f5b4b-106">Eine Warnmeldung ist ein modales Dialogfeld, eine direkte Nachricht, eine Benachrichtigung oder eine Sprechblase, die den Benutzer über eine Bedingung benachrichtigt, die möglicherweise in der Zukunft ein Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![Screenshot einer typischen Warnmeldung](images/mess-warn-image1.png)

<span data-ttu-id="f5b4b-108">Eine typische modale Warnmeldung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-108">A typical modal warning message.</span></span>

<span data-ttu-id="f5b4b-109">Das wichtigste Merkmal von Warnungen besteht darin, dass Sie das Risiko eines Verlusts von einem oder mehreren der folgenden Punkte einschließen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="f5b4b-110">Ein wertvolles Asset, z. b. wichtige Finanzdaten oder andere Daten.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="f5b4b-111">System Zugriff oder-Integrität.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-111">System access or integrity.</span></span>
-   <span data-ttu-id="f5b4b-112">Datenschutz oder Kontrolle über vertrauliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="f5b4b-113">Benutzer Zeit (eine beträchtliche Menge, z. b. 30 Sekunden oder mehr).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="f5b4b-114">Im Gegensatz dazu ist eine Bestätigung ein modales Dialogfeld, in dem Sie gefragt werden, ob der Benutzer eine Aktion fortsetzen möchte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="f5b4b-115">Einige Typen von Warnungen werden als Bestätigungen dargestellt, und wenn dies der Fall ist, gelten die Bestätigungs Richtlinien ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="f5b4b-116">**Hinweis:** Richtlinien, die sich auf [Dialogfelder](win-dialog-box.md), [Bestätigungen](mess-confirm.md), [Fehlermeldungen](mess-error.md)[Standardsymbole](vis-std-icons.md), [Benachrichtigungen](mess-notif.md)und das [Layout](vis-layout.md) beziehen, werden in separaten Artikeln dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="f5b4b-117">Handelt es sich um die richtige Benutzeroberfläche?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-117">Is this the right user interface?</span></span>

<span data-ttu-id="f5b4b-118">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="f5b4b-119">**Wird der Benutzer über eine Bedingung benachrichtigt, die in der Zukunft möglicherweise ein Problem verursacht?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="f5b4b-120">Andernfalls ist die Nachricht keine Warnung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="f5b4b-121">**Stellt die Benutzeroberfläche einen Fehler oder ein Problem dar, das bereits aufgetreten ist?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="f5b4b-122">Wenn dies der Fall ist, verwenden Sie stattdessen eine Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="f5b4b-123">**Werden Benutzer wahrscheinlich eine Aktion ausführen oder Ihr Verhalten als Ergebnis der Nachricht ändern?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="f5b4b-124">Wenn dies nicht der Fall ist, wird die Unterbrechung des Benutzers durch die Bedingung nicht rechtfertigen, sodass die Warnung besser unterdrückt werden kann</span><span class="sxs-lookup"><span data-stu-id="f5b4b-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="f5b4b-125">**Ist die Bedingung das direkte Ergebnis einer vom Benutzer initiierten Aktion?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="f5b4b-126">Wenn dies nicht der Fall ist, sollten Sie eine [nicht kritische Ereignis Benachrichtigung](mess-notif.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="f5b4b-127">**Handelt es sich bei der Bedingung um eine besondere Bedingung in einem Steuerelement?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="f5b4b-128">Verwenden Sie in diesem Fall [stattdessen eine](ctrl-balloons.md) Sprechblase.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="f5b4b-129">**Soll der Benutzer für Bestätigungen eine riskante Aktion ausführen?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="f5b4b-130">Wenn dies der Fall ist, ist eine Warnung geeignet, wenn die Aktion bedeutende Konsequenzen hat oder nicht einfach rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="f5b4b-131">**Für andere Typen von Warnungen muss der Benutzer jetzt oder in naher Zukunft agieren?**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="f5b4b-132">Zeigen Sie keine Warnungen an, wenn Benutzer ohne unmittelbare Probleme weiterhin produktiv arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="f5b4b-133">Verschieben Sie die Warnung so lange, bis die Bedingung unmittelbarer und relevanter ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="f5b4b-134">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="f5b4b-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="f5b4b-135">Vermeiden von überschreinungs Warnungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-135">Avoid overwarning</span></span>

<span data-ttu-id="f5b4b-136">Wir haben in Microsoft Windows-Programmen Vorrang vor der Warnung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="f5b4b-137">Das typische Windows-Programm weist scheinbar überall Warnungen auf, die mit einer geringen Bedeutung zu tun haben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="f5b4b-138">In einigen Programmen wird fast jede Frage als Warnung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="f5b4b-139">Durch die übermäßige Warnung wird die Verwendung eines Programms wie eine gefährliche Aktivität vereinfacht, und es wird von wirklich wichtigen Problemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="f5b4b-140">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-140">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-141">Screenshot einer unnötigen Warnmeldung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="f5b4b-142">Durch die übermäßige Warnung wird Ihr Programm gefährlich, und es sieht so aus, als ob es von Anwälten entworfen wurde</span><span class="sxs-lookup"><span data-stu-id="f5b4b-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="f5b4b-143">Das einzige Potenzial für Datenverluste oder ein zukünftiges Problem allein ist nicht ausreichend, um eine Warnung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="f5b4b-144">Außerdem sollten unerwünschte Ergebnisse unerwartet oder unbeabsichtigt sein und nicht einfach korrigiert werden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="f5b4b-145">Andernfalls können fast alle Benutzerfehler so interpretiert werden, dass Datenverluste oder potenzielle Probleme auftreten und eine Warnung ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="f5b4b-146">Merkmale von guten Warnungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-146">Characteristics of good warnings</span></span>

<span data-ttu-id="f5b4b-147">Gute Warnungen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-147">Good warnings:</span></span>

-   <span data-ttu-id="f5b4b-148">**Risiken einbeziehen.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-148">**Involve risk.**</span></span> <span data-ttu-id="f5b4b-149">Gute Warnungen warnen Benutzer von etwas signifikanter.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="f5b4b-150">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-150">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-151">Screenshot von "möchten Sie den Vorgang beenden?"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="f5b4b-152">warning</span><span class="sxs-lookup"><span data-stu-id="f5b4b-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="f5b4b-153">Na und?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-153">So what?</span></span> <span data-ttu-id="f5b4b-154">Diese Bestätigung setzt voraus, dass Benutzer Programme oft versehentlich beenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="f5b4b-155">**Sie haben unmittelbare Relevanz.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-155">**Have immediate relevance.**</span></span> <span data-ttu-id="f5b4b-156">Sie müssen sich nicht nur auf die Benutzer kümmern, sondern auch darauf achten.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="f5b4b-157">Benutzer sind in der Regel nicht an Problemen interessiert, die möglicherweise später auftreten, wenn Sie Ihre Arbeit jetzt erledigen können.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="f5b4b-158">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-158">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-159">Screenshot der Akku-Low-in-3-Stunden-Warnung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="f5b4b-160">In diesem Fall ist es besser, den Benutzer in drei Stunden zu warnen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="f5b4b-161">**Führt zu einer Aktion.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-161">**Lead to action.**</span></span> <span data-ttu-id="f5b4b-162">Es gibt etwas, das Benutzer als Ergebnis der Warnung verwenden oder beachten müssen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="f5b4b-163">Möglicherweise müssen Sie jetzt oder in der unmittelbaren Zukunft eine Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="f5b4b-164">Möglicherweise wird eine Aufgabe als Ergebnis anders durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="f5b4b-165">Die Folge, dass die Warnung ignoriert wird, sollte klar sein.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="f5b4b-166">Warnungen ohne Aktionen machen es einfach, dass die Benutzer in der Meinung sind</span><span class="sxs-lookup"><span data-stu-id="f5b4b-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="f5b4b-167">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-167">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-168">Screenshot der Warnung "Live Messenger wird ausgeführt"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="f5b4b-169">Warum ist diese Benachrichtigung eine Warnung?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-169">Why is this notification a warning?</span></span> <span data-ttu-id="f5b4b-170">Was sollten Benutzer tun (neben Sorge)?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="f5b4b-171">**Sind nicht offensichtlich.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-171">**Are not obvious.**</span></span> <span data-ttu-id="f5b4b-172">Zeigen Sie keine Warnung an, um die offensichtliche Folge einer Aktion anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="f5b4b-173">Nehmen Sie z. b. an, dass Benutzer die Konsequenzen der Nichtausführung einer Aufgabe verstehen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="f5b4b-174">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-174">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-175">Screenshot von möchten Sie den Assistenten beenden? davor</span><span class="sxs-lookup"><span data-stu-id="f5b4b-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="f5b4b-176">Wenn Sie einen unvollständigen Assistenten abbrechen, wird der Task nicht ausgeführt... Wer wusste?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="f5b4b-177">**Tritt selten auf.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-177">**Occur infrequently.**</span></span> <span data-ttu-id="f5b4b-178">Konstante Warnungen werden schnell wirkungslos und lästig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="f5b4b-179">Benutzer werden häufig stärker darauf ausgerichtet, die Warnung zu beseitigen, als das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="f5b4b-180">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-180">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-181">Screenshot der Warnung "Viren Signaturen aktualisieren"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="f5b4b-182">Benutzer sind eher darauf ausgerichtet, die Warnung zu entfernen, als das zugrunde liegende Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="f5b4b-183">Eine Nachricht, die nicht über diese Merkmale verfügt, ist möglicherweise trotzdem eine gute Nachricht, aber keine gute Warnung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="f5b4b-184">Bestimmen des geeigneten Nachrichten Typs</span><span class="sxs-lookup"><span data-stu-id="f5b4b-184">Determine the appropriate message type</span></span>

<span data-ttu-id="f5b4b-185">Einige Probleme können je nach Betonung und Formulierung als Fehler, Warnung oder Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="f5b4b-186">Nehmen Sie beispielsweise an, eine Webseite kann ein nicht signiertes ActiveX-Steuerelement nicht auf Grundlage der aktuellen Windows Internet Explorer-Konfiguration laden:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="f5b4b-187">**Zeit.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-187">**Error.**</span></span> <span data-ttu-id="f5b4b-188">"Auf dieser Seite kann kein nicht signiertes ActiveX-Steuerelement geladen werden."</span><span class="sxs-lookup"><span data-stu-id="f5b4b-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="f5b4b-189">(Als vorhandenes Problem formuliert.)</span><span class="sxs-lookup"><span data-stu-id="f5b4b-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="f5b4b-190">**Davor.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-190">**Warning.**</span></span> <span data-ttu-id="f5b4b-191">"Diese Seite verhält sich möglicherweise nicht wie erwartet, da Windows Internet Explorer nicht zum Laden von nicht signierten ActiveX-Steuerelementen konfiguriert ist."</span><span class="sxs-lookup"><span data-stu-id="f5b4b-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="f5b4b-192">oder "Diese Seite darf ein nicht signiertes ActiveX-Steuerelement installieren?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="f5b4b-193">Wenn Sie dies aus nicht vertrauenswürdigen Quellen machen, kann dies Ihren Computer beeinträchtigen. "</span><span class="sxs-lookup"><span data-stu-id="f5b4b-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="f5b4b-194">(Beide werden als Bedingungen formuliert, die möglicherweise zukünftige Probleme verursachen.)</span><span class="sxs-lookup"><span data-stu-id="f5b4b-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="f5b4b-195">**Informationen.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-195">**Information.**</span></span> <span data-ttu-id="f5b4b-196">"Sie haben Windows Internet Explorer so konfiguriert, dass nicht signierte ActiveX-Steuerelemente blockiert werden."</span><span class="sxs-lookup"><span data-stu-id="f5b4b-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="f5b4b-197">(Als eine-Anweisung formuliert.)</span><span class="sxs-lookup"><span data-stu-id="f5b4b-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="f5b4b-198">**Um den richtigen Nachrichtentyp zu bestimmen, konzentrieren Sie sich auf den wichtigsten Aspekt des Problems, das Benutzer kennen oder reagieren müssen.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="f5b4b-199">Wenn ein Problem darin besteht, dass der Benutzer nicht mehr fortfahren kann, sollten Sie es in der Regel als Fehler darstellen. Wenn der Benutzer fortfahren kann, stellen Sie ihn als Warnung dar.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="f5b4b-200">Erstellen Sie die [Haupt Anweisung](text-ui.md) oder einen anderen entsprechenden Text basierend auf diesem Fokus, und wählen Sie dann ein Symbol ([Standard](vis-std-icons.md) oder anderweitig), das mit dem Text übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="f5b4b-201">Der Hauptanweisungs Text und die Symbole sollten immer mit dem Text identisch sein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="f5b4b-202">Spezifisch</span><span class="sxs-lookup"><span data-stu-id="f5b4b-202">Be specific</span></span>

<span data-ttu-id="f5b4b-203">Warnungen sind überzeugender, wenn die folgenden Informationen spezifisch und klar sind:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="f5b4b-204">Die Quelle der Warnung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-204">The source of the warning.</span></span>
-   <span data-ttu-id="f5b4b-205">Die spezifische Bedingung und das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="f5b4b-206">Was der Benutzer damit tun sollte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-206">What the user should do about it.</span></span>
-   <span data-ttu-id="f5b4b-207">Was geschieht, wenn der Benutzer nichts tut.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="f5b4b-208">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-208">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-209">Screenshot der vagen Warnung mit erheblichem Risiko</span><span class="sxs-lookup"><span data-stu-id="f5b4b-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="f5b4b-210">In diesem Beispiel ist das potenzielle Problem?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="f5b4b-211">Was soll der Benutzer tun, abgesehen davon, dass er nicht den Projektor über das Netzwerk verwendet?</span><span class="sxs-lookup"><span data-stu-id="f5b4b-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="f5b4b-212">Ohne genauere Informationen kann der Vorgang nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="f5b4b-213">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-213">**Correct:**</span></span>

![<span data-ttu-id="f5b4b-214">Screenshot der Warnung zu Problemen und folgen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="f5b4b-215">In diesem Beispiel sind das Problem und die Konsequenzen eindeutig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="f5b4b-216">Manchmal gibt es ein legitimer potenzielles Problem, das die Benutzer über informiert, aber die Lösung und die Konsequenzen sind nicht bekannt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="f5b4b-217">Anstatt eine vage Warnung anzugeben, sollten Sie die wahrscheinlichsten Informationen oder das gängigste Beispiel bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="f5b4b-218">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-218">**Correct:**</span></span>

![<span data-ttu-id="f5b4b-219">Screenshot der Netzwerkfehler Warnung und-Lösungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="f5b4b-220">In diesem Beispiel wird die Warnung durch Bereitstellen der wahrscheinlichsten Lösung festgestellt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="f5b4b-221">Verwenden Sie in solchen Fällen jedoch einen Wortlaut, der angibt, dass andere Möglichkeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="f5b4b-222">Andernfalls werden Benutzer möglicherweise Irre geführt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="f5b4b-223">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-223">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-224">Screenshot der Warnung "Netzwerkkabel getrennt"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="f5b4b-225">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-225">**Correct:**</span></span>

![<span data-ttu-id="f5b4b-226">Screenshot des Kabels kann eine fehlende Warnung sein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="f5b4b-227">Im falschen Beispiel werden die Benutzer verwirrt, wenn das Kabel eindeutig angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="f5b4b-228">**Wenn Sie nur zwei Dinge tun...**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="f5b4b-229">Nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-229">Don't overwarn.</span></span> <span data-ttu-id="f5b4b-230">Beschränken Sie Warnungen auf Bedingungen, die ein Risiko darstellen und sofort relevant, handlungsfähig, nicht offensichtlich und selten sind.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="f5b4b-231">Andernfalls entfernen Sie die Nachricht, oder formulieren Sie Sie neu.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="f5b4b-232">Geben Sie spezielle, nützliche Informationen an.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="f5b4b-233">Verwendungsmuster</span><span class="sxs-lookup"><span data-stu-id="f5b4b-233">Usage patterns</span></span>

<span data-ttu-id="f5b4b-234">Warnungen weisen mehrere Verwendungs Muster auf:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5b4b-235"><strong>Bewusstsein</strong></span><span class="sxs-lookup"><span data-stu-id="f5b4b-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="f5b4b-236">Sorgen Sie dafür, dass der Benutzer eine Bedingung oder ein potenzielles Problem erkennt, aber der Benutzer muss möglicherweise noch nichts Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="f5b4b-237">Beispiele für Warnungen zu Warnungen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="f5b4b-238">Warnungen zu Warnungen haben folgende Präsentation:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="f5b4b-239"><strong>Main-Anweisung:</strong> Beschreiben Sie die Bedingung oder das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="f5b4b-240"><strong>Ergänzende Anweisung:</strong> Erläutern Sie die Implikation und warum Sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="f5b4b-241"><strong>Commit-Schaltflächen:</strong> Ihrer.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5b4b-242"><strong>Fehler Verhinderung</strong></span><span class="sxs-lookup"><span data-stu-id="f5b4b-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="f5b4b-243">Machen Sie die Benutzer auf Informationen aufmerksam, die möglicherweise ein Problem verhindern, insbesondere bei Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="f5b4b-244">Warnungen zur Fehler Verhinderung werden am besten mit einem direkten Warnsymbol und einem erklärenden Text dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="f5b4b-245">Beispiele für Warnungen zur Fehler Verhinderung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5b4b-246"><strong>Bevorstehendes Problem</strong></span><span class="sxs-lookup"><span data-stu-id="f5b4b-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="f5b4b-247">Der Benutzer muss jetzt etwas tun, um ein bevorstehendes Problem zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="f5b4b-248">Ein Beispiel für eine Warnung zu einem bevorstehenden Problem.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="f5b4b-249">Bevorstehende Problem Warnungen haben folgende Präsentation:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="f5b4b-250"><strong>Main-Anweisung:</strong> Beschreiben Sie, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="f5b4b-251"><strong>Ergänzende Anweisung:</strong> Erläutern Sie die Bedingung und warum Sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="f5b4b-252"><strong>Commit-Schaltflächen:</strong> Eine Befehls Schaltfläche oder ein Befehls Link für jede Option oder OK, wenn die Aktion außerhalb des Dialog Felds erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5b4b-253"><strong>Bestätigung der riskanten Aktion</strong></span><span class="sxs-lookup"><span data-stu-id="f5b4b-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="f5b4b-254">Vergewissern Sie sich, dass der Benutzer eine Aktion durchführen möchte, die ein gewisses Risiko aufweist und nicht einfach rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="f5b4b-255">Ein Beispiel für eine risikobehaftete Aktions Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="f5b4b-256">Riskante Aktions Bestätigungen haben die folgende Präsentation:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="f5b4b-257"><strong>Main-Anweisung:</strong> Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="f5b4b-258"><strong>Ergänzende Anweisung:</strong> Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="f5b4b-259"><strong>Commit-Schaltflächen:</strong> Ja, Nein.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="f5b4b-260">Richtlinien zu diesem Muster finden Sie unter <a href="mess-confirm.md">Bestätigungen</a>.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="f5b4b-261">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f5b4b-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="f5b4b-262">Präsentation</span><span class="sxs-lookup"><span data-stu-id="f5b4b-262">Presentation</span></span>

-   <span data-ttu-id="f5b4b-263">**Wählen Sie die Präsentations Benutzeroberfläche basierend auf der Art der Informationen aus:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-263">**Choose the presentation UI based on the type of information:**</span></span>



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b4b-264">**User interface (Benutzeroberfläche)**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-264">**User interface**</span></span><br/> | <span data-ttu-id="f5b4b-265">**Beste Verwendung für**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-265">**Best used for**</span></span><br/>                                                                                                           |
| <span data-ttu-id="f5b4b-266">Modale Dialogfelder</span><span class="sxs-lookup"><span data-stu-id="f5b4b-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="f5b4b-267">Kritische Warnungen (einschließlich Bestätigungen), auf die Benutzer jetzt Antworten müssen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="f5b4b-268">Direkt</span><span class="sxs-lookup"><span data-stu-id="f5b4b-268">In-place</span></span><br/>           | <span data-ttu-id="f5b4b-269">Informationen, die möglicherweise ein Problem verhindern, insbesondere, wenn Benutzer Entscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="f5b4b-270">Mitzubringen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-270">Banners</span></span><br/>            | <span data-ttu-id="f5b4b-271">Informationen, die möglicherweise ein Problem verhindern, insbesondere im Zusammenhang mit dem Abschließen einer Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="f5b4b-272">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-272">Notifications</span></span><br/>      | <span data-ttu-id="f5b4b-273">Wichtige Ereignisse oder Status, die auf sichere Weise ignoriert werden können, zumindest vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="f5b4b-274">Ballons</span><span class="sxs-lookup"><span data-stu-id="f5b4b-274">Balloons</span></span><br/>           | <span data-ttu-id="f5b4b-275">Ein-Steuerelement befindet sich in einem Zustand, der sich auf Eingaben auswirkt</span><span class="sxs-lookup"><span data-stu-id="f5b4b-275">A control is in a state that affects input.</span></span> <span data-ttu-id="f5b4b-276">Dieser Status ist wahrscheinlich unbeabsichtigt, und der Benutzer hat möglicherweise keine Eingaben erkannt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="f5b4b-277">**Für modale Dialogfelder:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="f5b4b-278">**Verwenden Sie nach Bedarf Aufgaben Dialogfelder, um ein konsistentes Aussehen und Layout zu erzielen.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="f5b4b-279">Aufgaben Dialogfelder erfordern Windows Vista oder höher, sodass Sie nicht für frühere Versionen von Windows geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="f5b4b-280">**Zeigt nur eine Warnmeldung pro Bedingung an.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="f5b4b-281">Zeigen Sie z. b. eine einzelne Warnung an, die eine Bedingung vollständig erläutert, anstatt Sie jeweils einmal pro Nachricht zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="f5b4b-282">Das Anzeigen einer Sequenz von Warn Dialogfeldern für eine einzelne Bedingung ist verwirrend und lästig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="f5b4b-283">**Zeigen Sie eine Warnung nicht mehr als einmal pro Bedingung an.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="f5b4b-284">Konstante Warnungen werden schnell wirkungslos und lästig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="f5b4b-285">Benutzer werden häufig stärker darauf ausgerichtet, die Warnung zu beseitigen, als das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="f5b4b-286">Wenn Sie für eine einzelne Bedingung wiederholt warnen müssen, verwenden Sie [Progressive Eskalation](mess-notif.md).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="f5b4b-287">**Führen Sie keine Warnungen mit einem Soundeffekt oder einem Signal aus.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="f5b4b-288">Dabei handelt es sich um jarringverfahren und unnötig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="f5b4b-289">**Ausnahme:** Wenn der Benutzer sofort Antworten muss, können Sie einen Soundeffekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="f5b4b-290">Symbole</span><span class="sxs-lookup"><span data-stu-id="f5b4b-290">Icons</span></span>

-   <span data-ttu-id="f5b4b-291">Platzieren Sie kein Warnsymbol in der Titelleiste eines Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="f5b4b-292">**Verwenden Sie ein Warnsymbol.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-292">**Use a warning icon.**</span></span> <span data-ttu-id="f5b4b-293">Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-293">Exceptions:</span></span>
    -   <span data-ttu-id="f5b4b-294">Wenn die Warnung für eine Funktion ist, die über ein Symbol verfügt, können Sie das Funktions Symbol mit einem Warn Überlagerungs Symbol verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="f5b4b-295">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-295">**Correct:**</span></span>

        ![<span data-ttu-id="f5b4b-296">Screenshot des sperrsymbols mit Warnsymbol Überlagerung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="f5b4b-297">In diesem Beispiel enthält das Feature-Symbol eine Warn Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="f5b4b-298">Legen Sie für modale Dialogfelder mit einer Warn fußnotiz das Warnsymbol in der fußnotiz anstelle des Inhalts Bereichs ab.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="f5b4b-299">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-299">**Correct:**</span></span>

    ![<span data-ttu-id="f5b4b-300">Screenshot des Warn Symbols im Dialogfeld "Fußnote"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="f5b4b-301">In diesem Beispiel enthält die fußnotiz das Warnsymbol.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="f5b4b-302">Weitere Richtlinien und Beispiele finden Sie unter [Standard Symbole](vis-std-icons.md).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="f5b4b-303">Diese Meldung nicht mehr anzeigen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-303">Don't show this message again</span></span>

-   <span data-ttu-id="f5b4b-304">**Wenn diese Option für ein Warn Dialogfeld erforderlich ist, überdenken Sie die Warnung und deren Häufigkeit.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="f5b4b-305">Wenn Sie über alle Merkmale einer guten Warnung verfügt (was ein Risiko darstellt und sofort relevant, handlungsfähig, nicht offensichtlich und unregelmäßig ist), sollte es für Benutzer nicht sinnvoll sein, Sie zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="f5b4b-306">Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="f5b4b-307">Schrittweise Offenlegung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-307">Progressive disclosure</span></span>

-   <span data-ttu-id="f5b4b-308">**Wenn Sie erweiterte Informationen in eine Warnmeldung einschließen müssen, können Sie diese mithilfe der Schaltflächen für die Progressive Offenlegung** anzeigen (z. b. "Details anzeigen").</span><span class="sxs-lookup"><span data-stu-id="f5b4b-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="f5b4b-309">Dies vereinfacht die Warnung für die typische Verwendung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="f5b4b-310">Blenden Sie erforderliche Informationen nicht aus, da Benutzer Sie möglicherweise nicht finden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="f5b4b-311">**Verwenden Sie "Details anzeigen" nicht, es sei denn, es gibt wirklich weitere Details.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="f5b4b-312">Geben Sie die vorhandenen Informationen nicht nur in einem anderen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="f5b4b-313">Informationen zu Bezeichnungs Richtlinien finden Sie unter [Progressive Offenlegung](ctrl-progressive-disclosure-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f5b4b-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="f5b4b-314">Standardwerte</span><span class="sxs-lookup"><span data-stu-id="f5b4b-314">Default values</span></span>

-   <span data-ttu-id="f5b4b-315">**Wählen Sie die sicherste, am wenigsten zerstörerische oder sicherste Antwort als Standard aus.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="f5b4b-316">Text</span><span class="sxs-lookup"><span data-stu-id="f5b4b-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="f5b4b-317">Allgemein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-317">General</span></span>

-   <span data-ttu-id="f5b4b-318">**Entfernen Sie den redundanten Text.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-318">**Remove redundant text.**</span></span> <span data-ttu-id="f5b4b-319">Suchen Sie nach dem Titel, den Haupt Anweisungen, zusätzlichen Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="f5b4b-320">Im Allgemeinen sollten Sie voll Text in Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="f5b4b-321">**Verwenden Sie nicht die Begriffe "Warnung" oder "Vorsicht" im Text.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="f5b4b-322">Wenn das Warnsymbol [ordnungsgemäß verwendet](vis-std-icons.md)wird, kommuniziert das Warnsymbol ausreichend, dass Benutzer mit Vorsicht fortfahren müssen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="f5b4b-323">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-323">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-324">Screenshot der unnötigen Verwendung von Warnung im Text</span><span class="sxs-lookup"><span data-stu-id="f5b4b-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="f5b4b-325">In diesem Beispiel ist der Begriff "Warning" nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="f5b4b-326">Titel</span><span class="sxs-lookup"><span data-stu-id="f5b4b-326">Titles</span></span>

-   <span data-ttu-id="f5b4b-327">**Verwenden Sie den Titel, um den Befehl oder das Feature zu identifizieren, von dem die Warnung stammt.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="f5b4b-328">Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-328">Exceptions:</span></span>
    -   <span data-ttu-id="f5b4b-329">Wenn eine Warnung von vielen verschiedenen Befehlen angezeigt wird, sollten Sie stattdessen den Programmnamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="f5b4b-330">Wenn der Titel mit der Main-Anweisung redundant oder verwirrend wäre, sollten Sie stattdessen den Programmnamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="f5b4b-331">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-331">**Incorrect:**</span></span>

![<span data-ttu-id="f5b4b-332">Screenshot des Dialogfeld Titels mit der Sicherheitswarnung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="f5b4b-333">In diesem Beispiel identifiziert "Sicherheitswarnung" nicht den Befehl oder das Feature, von dem die Warnung stammt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="f5b4b-334">**Verwenden Sie den Titel nicht, um zu erläutern, wie Sie im Dialog** Feld mit der Main-Anweisung vorgehen sollten.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="f5b4b-335">Verwenden Sie die Groß-/Kleinschreibung im [Titel](glossary.md), ohne die Beendigung zu beenden</span><span class="sxs-lookup"><span data-stu-id="f5b4b-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="f5b4b-336">Haupt Anleitung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-336">Main instructions</span></span>

-   <span data-ttu-id="f5b4b-337">Die Haupt Anweisung für eine Warnung basiert auf dem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-337">The main instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="f5b4b-338">**Muster**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-338">**Pattern**</span></span><br/>               | <span data-ttu-id="f5b4b-339">**Main-Anweisung**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-339">**Main instruction**</span></span><br/>                                      |
| <span data-ttu-id="f5b4b-340">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-340">Awareness</span></span><br/>                 | <span data-ttu-id="f5b4b-341">Beschreiben Sie die Bedingung oder das potenzielle Problem.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="f5b4b-342">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="f5b4b-342">Imminent problem</span></span><br/>          | <span data-ttu-id="f5b4b-343">Beschreiben Sie, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="f5b4b-344">Bestätigung der riskanten Aktion</span><span class="sxs-lookup"><span data-stu-id="f5b4b-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="f5b4b-345">Stellen Sie eine Frage, um zu bestimmen, ob der Benutzer den Vorgang fortsetzen möchte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="f5b4b-346">Screenshot einer Benachrichtigung mit geringem Akku</span><span class="sxs-lookup"><span data-stu-id="f5b4b-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="f5b4b-347">In diesem Beispiel ist die Benachrichtigung bei geringer Akku Benachrichtigung eine Warnung, sodass die Bedingung in der Haupt Anweisung beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="f5b4b-348">Screenshot der Änderung der Akku sofortige Warnung</span><span class="sxs-lookup"><span data-stu-id="f5b4b-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="f5b4b-349">In diesem Beispiel ist das Dialogfeld "geringe Akkukapazität" ein bevorstehendes Problem, daher wird in der Haupt Anweisung beschrieben, was der Benutzer jetzt tun muss.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="f5b4b-350">**Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="f5b4b-351">Entfernen Sie die Haupt Anweisung zu den wesentlichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="f5b4b-352">Wenn Sie etwas anderes erläutern müssen, verwenden Sie eine ergänzende Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="f5b4b-353">**Verwenden Sie Wörter wie "Now" und "sofort", wenn der Benutzer sofort agieren muss.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="f5b4b-354">Verwenden Sie diese Wörter nicht, wenn es keine Dringlichkeit gibt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="f5b4b-355">**Wenn Objekte beteiligt sind, geben Sie die vollständigen Namen an.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="f5b4b-356">Verwenden Sie die Groß Schreibung im [Satz](glossary.md)Format.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="f5b4b-357">Ergänzende Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-357">Supplemental instructions</span></span>

-   <span data-ttu-id="f5b4b-358">Die ergänzende Anweisung für eine Warnung basiert auf dem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b4b-359">**Muster**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-359">**Pattern**</span></span><br/>               | <span data-ttu-id="f5b4b-360">**Ergänzende Anweisung**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-360">**Supplemental instruction**</span></span><br/>                                            |
| <span data-ttu-id="f5b4b-361">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-361">Awareness</span></span><br/>                 | <span data-ttu-id="f5b4b-362">Erläutern Sie die Implikation und warum Sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="f5b4b-363">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="f5b4b-363">Imminent problem</span></span><br/>          | <span data-ttu-id="f5b4b-364">Erläutern Sie die Bedingung und warum Sie wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="f5b4b-365">Bestätigung der riskanten Aktion</span><span class="sxs-lookup"><span data-stu-id="f5b4b-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="f5b4b-366">Erläutern Sie alle nicht offensichtlichen Gründe, warum der Benutzer möglicherweise nicht fortfahren möchte.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="f5b4b-367">**Wiederholen Sie die main-Anweisung nicht mit etwas anderen Formulierungen.**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="f5b4b-368">Lassen Sie stattdessen die ergänzende Anweisung Weg, wenn nicht mehr hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="f5b4b-369">Verwenden Sie vollständige Sätze, die Groß-/Kleinschreibung und die endinterpunktions Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="f5b4b-370">Commit-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="f5b4b-370">Commit buttons</span></span>

-   <span data-ttu-id="f5b4b-371">Für Warn Dialogfelder basieren die Commit-Schaltflächen auf dem Entwurfsmuster:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b4b-372">**Muster**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-372">**Pattern**</span></span><br/>               | <span data-ttu-id="f5b4b-373">**Commit-Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-373">**Commit buttons**</span></span><br/>                                                                                   |
| <span data-ttu-id="f5b4b-374">Bewusstsein</span><span class="sxs-lookup"><span data-stu-id="f5b4b-374">Awareness</span></span><br/>                 | <span data-ttu-id="f5b4b-375">Fast richtig.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-375">Close.</span></span> <span data-ttu-id="f5b4b-376">Verwenden Sie "OK" nicht, da es ein mögliches Problem ist.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="f5b4b-377">Bevorstehendes Problem</span><span class="sxs-lookup"><span data-stu-id="f5b4b-377">Imminent problem</span></span><br/>          | <span data-ttu-id="f5b4b-378">Eine Befehls Schaltfläche oder ein Befehls Link für jede Option oder OK, wenn die Aktion außerhalb des Dialog Felds erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="f5b4b-379">Bestätigung der riskanten Aktion</span><span class="sxs-lookup"><span data-stu-id="f5b4b-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="f5b4b-380">Ja, Nein.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="f5b4b-381">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="f5b4b-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="f5b4b-382">Screenshot des Warn Dialogfelds mit der Schaltfläche "OK"</span><span class="sxs-lookup"><span data-stu-id="f5b4b-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="f5b4b-383">Probleme sind nicht in Ordnung. verwenden Sie daher stattdessen close.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="f5b4b-384">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="f5b4b-384">Documentation</span></span>

<span data-ttu-id="f5b4b-385">Beim Verweis auf Warnungen:</span><span class="sxs-lookup"><span data-stu-id="f5b4b-385">When referring to warnings:</span></span>

-   <span data-ttu-id="f5b4b-386">Wenn in der Warnung eine Frage gestellt wird, finden Sie eine Warnung nach Ihrer Frage. Andernfalls verwenden Sie die main-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="f5b4b-387">Wenn die Frage oder die Haupt Anweisung lang oder ausführlich ist, fassen Sie sie zusammen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="f5b4b-388">Falls erforderlich, können Sie auf ein Warn Dialogfeld als Nachricht verweisen.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="f5b4b-389">Formatieren Sie den Text nach Möglichkeit fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-389">When possible, format the text using bold.</span></span> <span data-ttu-id="f5b4b-390">Andernfalls sollten Sie den Text nur bei Bedarf in Anführungszeichen setzen, um Verwechslungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="f5b4b-391">Beispiel: Klicken Sie in der Meldung möchten **Sie die nicht sicheren Elemente anzeigen?** auf Ja.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

