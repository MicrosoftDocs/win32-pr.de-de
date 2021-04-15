---
title: Stil und Ton
description: Der Ton beim Schreiben ist die Haltung, die der Writer dem Reader überträgt.
ms.assetid: b9a03709-301f-46de-b4b4-0dd1214c0ed7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6009491b54de9035b253a10b9fd48f2233947104
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554203"
---
# <a name="style-and-tone"></a><span data-ttu-id="1f016-103">Stil und Ton</span><span class="sxs-lookup"><span data-stu-id="1f016-103">Style and Tone</span></span>

> [!NOTE]
> <span data-ttu-id="1f016-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1f016-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="1f016-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="1f016-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="1f016-106">Der Ton beim Schreiben ist die Haltung, die der Writer dem Reader überträgt.</span><span class="sxs-lookup"><span data-stu-id="1f016-106">Tone in writing is the attitude that the writer conveys to the reader.</span></span> <span data-ttu-id="1f016-107">Es ist nicht unbedingt das, was Sie sagen, sondern wie Sie es sagen.</span><span class="sxs-lookup"><span data-stu-id="1f016-107">It's not necessarily what you say, but how you say it.</span></span> <span data-ttu-id="1f016-108">Der Ton dient zum Erstellen einer bestimmten Antwort oder Emotionen im Reader. Es wird eine Persönlichkeit erstellt, die Benutzer einbinden oder repliell kann.</span><span class="sxs-lookup"><span data-stu-id="1f016-108">Tone is intended to create a specific response or emotion in the reader; it creates a personality that can either engage or repel users.</span></span>

<span data-ttu-id="1f016-109">**Hinweis:** Richtlinien im Zusammenhang mit dem [Text der Benutzeroberfläche](text-ui.md) werden in einem separaten Artikel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1f016-109">**Note:** Guidelines related to [user interface text](text-ui.md) are presented in a separate article.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="1f016-110">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="1f016-110">Design concepts</span></span>

### <a name="the-windows-tone"></a><span data-ttu-id="1f016-111">Der Windows-Ton</span><span class="sxs-lookup"><span data-stu-id="1f016-111">The Windows tone</span></span>

<span data-ttu-id="1f016-112">Verwenden Sie den Windows-Ton, um Vertrauen zu gewinnen, indem Sie den Benutzern auf persönlicher Ebene Vertrauen, indem Sie genau, ermutigend, aufschlussreich, Ziel und Benutzer orientiert sind.</span><span class="sxs-lookup"><span data-stu-id="1f016-112">Use the Windows tone to inspire confidence by communicating to users on a personal level by being accurate, encouraging, insightful, objective, and user focused.</span></span> <span data-ttu-id="1f016-113">Der Windows-Ton zielt auch darauf ab, leicht, inspirierend, unkompliziert und vertrauenswürdig zu sein.</span><span class="sxs-lookup"><span data-stu-id="1f016-113">The Windows tone also strives to be light, inspiring, straightforward, and trustworthy.</span></span>

<span data-ttu-id="1f016-114">Verwenden Sie keinen ablenkend-, absteigenden oder arroganten Ton.</span><span class="sxs-lookup"><span data-stu-id="1f016-114">Don't use a distracting, condescending, or arrogant tone.</span></span> <span data-ttu-id="1f016-115">Vermeiden Sie die Extreme der "Machine"-Stimme (bei der der Redner aus der Sprache entfernt wurde) und die Stimme des Vertriebsmitarbeiters (bei der das Schreiben versucht, uns etwas zu verkaufen, an cajole US.</span><span class="sxs-lookup"><span data-stu-id="1f016-115">Avoid the extremes of the "machine" voice (where the speaker is removed from the language) and the "sales rep" voice (where the writing tries to sell us something, to cajole us, to cheer us up, to gloss over everything as "simple.")</span></span>

<span data-ttu-id="1f016-116">Research von Microsoft zeigt, dass es in der Software häufig:</span><span class="sxs-lookup"><span data-stu-id="1f016-116">Research from Microsoft shows that in software, there is often:</span></span>

-   <span data-ttu-id="1f016-117">**Über Verwendung von Computerterminologie und-Fachjargon,** die viele Benutzer nicht verstehen oder interpretieren.</span><span class="sxs-lookup"><span data-stu-id="1f016-117">**Overuse of computer terminology and jargon,** which many users don't understand or misinterpret.</span></span>
-   <span data-ttu-id="1f016-118">**Inkonsistente Verwendung der Terminologie.**</span><span class="sxs-lookup"><span data-stu-id="1f016-118">**Inconsistent use of terminology.**</span></span>
-   <span data-ttu-id="1f016-119">**Unveränderlich, häufig versehentlich patronier Nachrichten,** die die Benutzer zum Entschlüsseln kämpfen.</span><span class="sxs-lookup"><span data-stu-id="1f016-119">**Impenetrable, often unintentionally patronizing messages,** which users struggle to decipher.</span></span>

<span data-ttu-id="1f016-120">Diese Probleme sorgen dafür, dass Benutzer verwirrend, unintelligent, unproblematisch und letztendlich von ihrer Erfahrung mit Software entzaubert werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-120">These problems make users feel confused, unintelligent, disheartened, and ultimately disengaged from their experience with software.</span></span>

<span data-ttu-id="1f016-121">Die neue Aufmerksamkeit auf die Nachrichten Qualität, einschließlich des Texts des Texts, impliziert, dass die Sprache selbst ein wichtiger Bestandteil der Kundenzufriedenheit ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-121">Renewed attention to message quality, including the tone of the text, implies that language itself is an important ingredient in overall customer satisfaction.</span></span> <span data-ttu-id="1f016-122">Unterstützen Sie Benutzer mit unterschiedlichen technischen Kenntnissen, insbesondere bei Einsteiger, damit Sie von den Vorteilen Ihres Programms profitieren können.</span><span class="sxs-lookup"><span data-stu-id="1f016-122">Support users with different levels of technical knowledge, especially novice users, to take advantage of all the things your program can do.</span></span>

<span data-ttu-id="1f016-123">**Wenn Sie nur eine Aktion ausführen...**</span><span class="sxs-lookup"><span data-stu-id="1f016-123">**If you do only one thing...**</span></span>

<span data-ttu-id="1f016-124">Stellen Sie sicher, dass Ihr Text genau, ermutigend, aufschlussreich, Ziel und Benutzer orientiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-124">Make sure that your text is accurate, encouraging, insightful, objective, and user-focused.</span></span> <span data-ttu-id="1f016-125">Seien Sie unkompliziert und vertrauenswürdig, und verwenden Sie bei Bedarf einen hellen und inspirierenden Ton.</span><span class="sxs-lookup"><span data-stu-id="1f016-125">Be straightforward and trustworthy, and where appropriate use a light and inspiring tone.</span></span>

## <a name="guidelines"></a><span data-ttu-id="1f016-126">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="1f016-126">Guidelines</span></span>

### <a name="use-the-windows-tone"></a><span data-ttu-id="1f016-127">Windows-Ton verwenden</span><span class="sxs-lookup"><span data-stu-id="1f016-127">Use the Windows tone</span></span>

<span data-ttu-id="1f016-128">Der Ton in Ihrem Programm sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="1f016-128">Tone in your program should be:</span></span>

-   <span data-ttu-id="1f016-129">**Präzi.**</span><span class="sxs-lookup"><span data-stu-id="1f016-129">**Accurate.**</span></span> <span data-ttu-id="1f016-130">Benutzer sollten sich sicher sein, dass die Informationen technisch genau sind.</span><span class="sxs-lookup"><span data-stu-id="1f016-130">Users should feel reassured that the information is technically accurate.</span></span> <span data-ttu-id="1f016-131">Wenn die Informationen nicht exakt sind, ist die Benutzeroberflächen Funktion für diese spezielle Aufgabe verdorben, und Sie verliert den Glauben an jede andere Unterstützung, die er aus dieser Quelle liest.</span><span class="sxs-lookup"><span data-stu-id="1f016-131">If the information isn't accurate, the user's experience with that specific task is spoiled, and he loses faith in any other assistance he reads from that source.</span></span>
-   <span data-ttu-id="1f016-132">**Dere.**</span><span class="sxs-lookup"><span data-stu-id="1f016-132">**Encouraging.**</span></span> <span data-ttu-id="1f016-133">Verwenden Sie die Sprache, mit der die Software den Benutzern ermöglicht wird, Dinge zu erledigen, anstatt Sie zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="1f016-133">Use language that conveys that the software empowers users to do things, rather than allows them to do things.</span></span> <span data-ttu-id="1f016-134">Verwenden Sie z. b. "Sie können" statt "Windows ermöglicht Ihnen" oder "Diese Funktion ermöglicht Ihnen".</span><span class="sxs-lookup"><span data-stu-id="1f016-134">For example, use "you can" rather than "Windows lets you" or "this feature allows you."</span></span> <span data-ttu-id="1f016-135">(Ausnahme: Es ist in Ordnung, "zulassen" zu verwenden, wenn auf Features verwiesen wird – z. b. Sicherheitsfeatures –, die eine Aktion zulassen oder verweigern.)</span><span class="sxs-lookup"><span data-stu-id="1f016-135">(Exception: it's okay to use "allow" when referring to features—such as security features—that permit or deny an action.)</span></span>
-   <span data-ttu-id="1f016-136">**Aufschlussreiche.**</span><span class="sxs-lookup"><span data-stu-id="1f016-136">**Insightful.**</span></span> <span data-ttu-id="1f016-137">Benutzer sollten der Meinung sein, dass Sie (und durch Erweiterung Ihrer Anwendung) wissen, wann eine bestimmte Aufgabe kompliziert ist und Sie durch Sie geführt werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-137">Users should believe that you (and by extension your application) know when a certain task is complicated and that you will guide them through it.</span></span> <span data-ttu-id="1f016-138">Gleichzeitig sollten Sie Benutzer als intelligente Personen behandeln, die Unterstützung für ein bestimmtes Problem benötigen.</span><span class="sxs-lookup"><span data-stu-id="1f016-138">At the same time, treat users as intelligent people who happen to need help with a particular problem.</span></span>
-   <span data-ttu-id="1f016-139">**Objektiver.**</span><span class="sxs-lookup"><span data-stu-id="1f016-139">**Objective.**</span></span> <span data-ttu-id="1f016-140">Manchmal möchten die Benutzer eine umfassendere Erläuterung erhalten. Häufig möchten Sie aber nur wissen, was Sie benötigen, um fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="1f016-140">Sometimes users want a richer explanation; often though they just want to know what they need to move on.</span></span> <span data-ttu-id="1f016-141">Dies erfordert eine Objektivität –, um zu erkennen, dass das Ziel (Produktivität, Neugier, Genuss) das Ziel des Benutzers ist, nicht die des Writers.</span><span class="sxs-lookup"><span data-stu-id="1f016-141">This requires objectivity—to recognize that the goal (productivity, curiosity, enjoyment) is the user's goal, not the writer's.</span></span> <span data-ttu-id="1f016-142">Außerdem ist es erforderlich, dass Sie alle vorab freigegebenen Vorstellungen über den Benutzer ablegen.</span><span class="sxs-lookup"><span data-stu-id="1f016-142">It also requires that you shed any predisposed notions about the user.</span></span>
-   <span data-ttu-id="1f016-143">**Benutzer orientiert.**</span><span class="sxs-lookup"><span data-stu-id="1f016-143">**User-focused.**</span></span> <span data-ttu-id="1f016-144">Schreiben Sie aus der Perspektive des Benutzers und vorzugsweise aus der Sicht, was Sie für den Benutzer tun können.</span><span class="sxs-lookup"><span data-stu-id="1f016-144">Write from the user's perspective and preferably from the perspective of what you can do for the user.</span></span> <span data-ttu-id="1f016-145">Benutzer werden feststellen, dass Sie Informationen finden, die für Sie relevant und zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="1f016-145">Users should feel that they will find information that is relevant and accessible to them.</span></span>

<span data-ttu-id="1f016-146">Sie können die Kommunikation mit ihren Benutzern weiterentwickeln, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="1f016-146">You can further develop communication with your users by being:</span></span>

-   <span data-ttu-id="1f016-147">**Grün.**</span><span class="sxs-lookup"><span data-stu-id="1f016-147">**Light.**</span></span> <span data-ttu-id="1f016-148">Eine helle Stimme ist einfach zu behandeln und schnell zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="1f016-148">A light voice feels easy to deal with and quick to comprehend.</span></span> <span data-ttu-id="1f016-149">Dies ist nicht schwierig oder schwer zu vermeiden, und es wird vermieden, dass eine Tiefe oder schwerwiegende Belastung ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-149">It isn't difficult or burdensome, and it avoids straining to be profound or serious.</span></span>
-   <span data-ttu-id="1f016-150">**Inspirierende.**</span><span class="sxs-lookup"><span data-stu-id="1f016-150">**Inspiring.**</span></span> <span data-ttu-id="1f016-151">Eine inspirierende Stimme motiviert Benutzer und fördert Sie, damit Sie Maßnahmen ergreifen können.</span><span class="sxs-lookup"><span data-stu-id="1f016-151">An inspiring voice motivates users, stimulating them to take action.</span></span> <span data-ttu-id="1f016-152">Eine bestimmte Begeisterung markiert diese Art von Stimme, sodass Sie eine ansprechende Persönlichkeit bietet, als die Benutzer, die häufig von ihren Computern erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-152">A certain enthusiasm marks this kind of voice, giving it a more engaging personality than the machine-like tone users have often come to expect from their computers.</span></span>
-   <span data-ttu-id="1f016-153">**Direkte.**</span><span class="sxs-lookup"><span data-stu-id="1f016-153">**Straightforward.**</span></span> <span data-ttu-id="1f016-154">Eine unkomplizierte Stimme ist "offene" und "Open", von der vorab-oder Betrugs freie Sprache.</span><span class="sxs-lookup"><span data-stu-id="1f016-154">A straightforward voice is candid and open, free from pretense or deceit.</span></span>
-   <span data-ttu-id="1f016-155">**Zuverlässigen.**</span><span class="sxs-lookup"><span data-stu-id="1f016-155">**Trustworthy.**</span></span> <span data-ttu-id="1f016-156">Eine vertrauenswürdige Stimme ist vertrauenswürdig, zuverlässig, genau und ehrlich.</span><span class="sxs-lookup"><span data-stu-id="1f016-156">A trustworthy voice is worthy of confidence, reliable, accurate, and honest.</span></span> <span data-ttu-id="1f016-157">Es dauert nur wenige Ungenauigkeiten, um die Vertrauenswürdigkeit des Benutzers zu verlieren, aber es kann sehr lange dauern, bis diese Vertrauensstellung wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="1f016-157">It only takes only a few inaccuracies to lose the user's trust, but it may take a long time to earn that trust back.</span></span>

<span data-ttu-id="1f016-158">Stellen Sie im Gegensatz dazu sicher, dass Sie die folgenden Töne vermeiden, die mit höherer Wahrscheinlichkeit eine negative Reaktion erhalten:</span><span class="sxs-lookup"><span data-stu-id="1f016-158">By contrast, be sure to avoid the following tones, which are much more likely to receive a negative reaction:</span></span>

-   <span data-ttu-id="1f016-159">**Computerton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-159">**Machine tone.**</span></span> <span data-ttu-id="1f016-160">Sie haben einen unpersönlichen, unflexiblen Austausch mit einem Computer oder Roboter.</span><span class="sxs-lookup"><span data-stu-id="1f016-160">Feels like having an impersonal, inflexible exchange with a computer or robot.</span></span>
-   <span data-ttu-id="1f016-161">**Unternehmenston.**</span><span class="sxs-lookup"><span data-stu-id="1f016-161">**Corporate tone.**</span></span> <span data-ttu-id="1f016-162">Sie haben einen Monolog mit einer vollständig leistungsfähigen, nicht persönlichen Corporation.</span><span class="sxs-lookup"><span data-stu-id="1f016-162">Feels like having a monologue with an all-powerful, all-knowing, impersonal corporation.</span></span>
-   <span data-ttu-id="1f016-163">**Strafverfolgungs-Ton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-163">**Law enforcement tone.**</span></span> <span data-ttu-id="1f016-164">Es hat sich gewünscht, dass Sie mit einer Flut von eindringlichen Fragen abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-164">Feels like being interrogated with a barrage of intrusive questions.</span></span>
-   <span data-ttu-id="1f016-165">**Lawyerly-Ton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-165">**Lawyerly tone.**</span></span> <span data-ttu-id="1f016-166">Es ist so, als ob Sie dazu aufgefordert werden, einen rechts wichtigen Act auszuführen</span><span class="sxs-lookup"><span data-stu-id="1f016-166">Feels like being asked to perform some legally significant act.</span></span>
-   <span data-ttu-id="1f016-167">**Vertriebsmitarbeiter.**</span><span class="sxs-lookup"><span data-stu-id="1f016-167">**Sales rep tone.**</span></span> <span data-ttu-id="1f016-168">Sie werden aufgefordert, etwas zu kaufen oder auszuprobieren, bei dem es darum geht, etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="1f016-168">Feels like being asked to buy or try something, with any concerns being glossed over.</span></span>
-   <span data-ttu-id="1f016-169">**Übergeordnetes, absteigende oder zornige Ton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-169">**Superior, condescending, or angry tone.**</span></span> <span data-ttu-id="1f016-170">Der Meinung nach ist, dass die Software Benutzer absinkt, sich mit Ihnen in Zusammenhang setzen oder mit Ihnen verärgert ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-170">Feels like the software is belittling users, talking down to them, or upset with them.</span></span> <span data-ttu-id="1f016-171">In der Regel ist dieser Farbton sehr technisch, setzt unnötige Aufmerksamkeit auf die Fehler des Benutzers und spürt ungrob.</span><span class="sxs-lookup"><span data-stu-id="1f016-171">Typically, this tone is very technical, draws unnecessary attention to the user's mistakes, and feels rude.</span></span>
-   <span data-ttu-id="1f016-172">**Boastiger Ton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-172">**Boastful tone.**</span></span> <span data-ttu-id="1f016-173">Der Meinung nach ist, dass die Software an sich über die zugehörigen Leistungen Meriten ist</span><span class="sxs-lookup"><span data-stu-id="1f016-173">Feels like the software is bragging about its accomplishments or otherwise drawing too much attention to itself.</span></span>
-   <span data-ttu-id="1f016-174">**Flippanter Ton.**</span><span class="sxs-lookup"><span data-stu-id="1f016-174">**Flippant tone.**</span></span> <span data-ttu-id="1f016-175">Sie fühlen sich wie die Ziele der Benutzer, oder die Emotionen werden nicht ernst genommen, oder die Verwendung des Programms wird gewährt.</span><span class="sxs-lookup"><span data-stu-id="1f016-175">Feels like users' goals and emotions aren't being taken seriously, or their use of the program is being take for granted.</span></span>

### <a name="use-real-world-language"></a><span data-ttu-id="1f016-176">Reale Sprache verwenden</span><span class="sxs-lookup"><span data-stu-id="1f016-176">Use real-world language</span></span>

-   <span data-ttu-id="1f016-177">**Verwenden Sie alltägliche Wörter, wenn Sie Wörter haben, die Sie nicht an andere Personen weitergibt.**</span><span class="sxs-lookup"><span data-stu-id="1f016-177">**Use everyday words when you can and avoid words you wouldn't say to someone else in person.**</span></span> <span data-ttu-id="1f016-178">Dies ist insbesondere dann effektiv, wenn Sie ein komplexes technisches Konzept oder eine komplexe Maßnahme erläutern.</span><span class="sxs-lookup"><span data-stu-id="1f016-178">This is especially effective if you are explaining a complex technical concept or action.</span></span> <span data-ttu-id="1f016-179">Stellen Sie sich vor, dass Sie sich die Schulter des Benutzers ansehen und erläutern, wie Sie die Aufgabe erledigen können.</span><span class="sxs-lookup"><span data-stu-id="1f016-179">Imagine yourself looking over the user's shoulder and explaining how to accomplish the task.</span></span>

    <span data-ttu-id="1f016-180">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-180">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-181">Verwenden Sie dieses Verfahren, um Ihr Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f016-181">Use this procedure to change your password.</span></span>

    <span data-ttu-id="1f016-182">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-182">**Better:**</span></span>

    <span data-ttu-id="1f016-183">Führen Sie diese Schritte aus, um Ihr Kennwort zu ändern</span><span class="sxs-lookup"><span data-stu-id="1f016-183">Follow these steps to change your password.</span></span>

-   <span data-ttu-id="1f016-184">**Verwenden Sie nach Möglichkeit kurze, einfache Wörter.**</span><span class="sxs-lookup"><span data-stu-id="1f016-184">**Use short, plain words whenever possible.**</span></span> <span data-ttu-id="1f016-185">Kürzere Wörter sind eher konverational, sparen Sie Speicherplatz auf dem Bildschirm und sind einfacher zu scannen.</span><span class="sxs-lookup"><span data-stu-id="1f016-185">Shorter words are more conversational, save space on screen, and are easier to scan.</span></span>

    <span data-ttu-id="1f016-186">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-186">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-187">Außerdem wird in diesem Abschnitt angezeigt...</span><span class="sxs-lookup"><span data-stu-id="1f016-187">In addition, this section shows you...</span></span>

    <span data-ttu-id="1f016-188">Digitale Kameras verwenden kleine Mikrochips...</span><span class="sxs-lookup"><span data-stu-id="1f016-188">Digital cameras employ tiny microchips...</span></span>

    <span data-ttu-id="1f016-189">Digitale Kameras verwenden kleine Mikrochips...</span><span class="sxs-lookup"><span data-stu-id="1f016-189">Digital cameras utilize tiny microchips...</span></span>

    <span data-ttu-id="1f016-190">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-190">**Better:**</span></span>

    <span data-ttu-id="1f016-191">Dieser Abschnitt zeigt Ihnen auch...</span><span class="sxs-lookup"><span data-stu-id="1f016-191">This section also shows you...</span></span>

    <span data-ttu-id="1f016-192">Digitale Kameras verwenden kleine Mikrochips...</span><span class="sxs-lookup"><span data-stu-id="1f016-192">Digital cameras use tiny microchips...</span></span>

-   <span data-ttu-id="1f016-193">**Sie sollten keine Wörter erfinden oder neue Bedeutungen auf Standard Wörter anwenden.**</span><span class="sxs-lookup"><span data-stu-id="1f016-193">**Don't invent words or apply new meanings to standard words.**</span></span> <span data-ttu-id="1f016-194">Nehmen Sie an, dass Benutzer besser mit der Bedeutung eines Worts vertraut sind als mit einer besonderen Bedeutung, die von der Technologiebranche angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1f016-194">Assume that users are more familiar with a word's established meaning than with a special meaning given it by the technology industry.</span></span> <span data-ttu-id="1f016-195">Wenn ein Branchen Begriff erforderlich ist, stellen Sie eine kontextbasierte Definition bereit.</span><span class="sxs-lookup"><span data-stu-id="1f016-195">When an industry term is required, provide an in-context definition.</span></span> <span data-ttu-id="1f016-196">Vermeiden Sie den Fachjargon, aber denken Sie daran, dass einige Ausdrücke, die für die Computer Verwendung – Hacker, Burn a CD usw. –, bereits Teil der alltäglichen Sprache sind.</span><span class="sxs-lookup"><span data-stu-id="1f016-196">Avoid jargon, but remember that some expressions specific to computer usage—hacker, burn a CD, and so on—are already part of everyday speech.</span></span>

    <span data-ttu-id="1f016-197">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="1f016-197">**Incorrect:**</span></span>

    <span data-ttu-id="1f016-198">Sie können Ordner verwenden, um Ihre Favoriten zu bucktieren.</span><span class="sxs-lookup"><span data-stu-id="1f016-198">You can use folders to bucketize your favorites.</span></span>

    <span data-ttu-id="1f016-199">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-199">**Correct:**</span></span>

    <span data-ttu-id="1f016-200">Sie können Ordner verwenden, um die Favoriten zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="1f016-200">You can use folders to categorize your favorites.</span></span>

-   <span data-ttu-id="1f016-201">**Verwenden Sie Symbole nicht als Ersatz für einfache Wörter.**</span><span class="sxs-lookup"><span data-stu-id="1f016-201">**Don't use symbols as a substitute for simple words.**</span></span>

    <span data-ttu-id="1f016-202">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="1f016-202">**Incorrect:**</span></span>

    <span data-ttu-id="1f016-203">Benutzer & Computer</span><span class="sxs-lookup"><span data-stu-id="1f016-203">users & computers</span></span>

    <span data-ttu-id="1f016-204">Benutzer und Computer</span><span class="sxs-lookup"><span data-stu-id="1f016-204">users + computers</span></span>

    <span data-ttu-id="1f016-205">Domäne/Arbeitsgruppe</span><span class="sxs-lookup"><span data-stu-id="1f016-205">domain / workgroup</span></span>

    <span data-ttu-id="1f016-206">\# von Benutzern</span><span class="sxs-lookup"><span data-stu-id="1f016-206">\# of users</span></span>

    <span data-ttu-id="1f016-207">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-207">**Correct:**</span></span>

    <span data-ttu-id="1f016-208">Benutzer und Computer</span><span class="sxs-lookup"><span data-stu-id="1f016-208">users and computers</span></span>

    <span data-ttu-id="1f016-209">Domäne oder Arbeitsgruppe</span><span class="sxs-lookup"><span data-stu-id="1f016-209">domain or workgroup</span></span>

    <span data-ttu-id="1f016-210">Anzahl der Benutzer</span><span class="sxs-lookup"><span data-stu-id="1f016-210">number of users</span></span>

### <a name="be-precise"></a><span data-ttu-id="1f016-211">Genaue Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="1f016-211">Be precise</span></span>

-   <span data-ttu-id="1f016-212">Wählen Sie Wörter aus, die eine klare Bedeutung haben.</span><span class="sxs-lookup"><span data-stu-id="1f016-212">Choose words with a clear meaning.</span></span>

    <span data-ttu-id="1f016-213">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-213">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-214">Da Sie die Tabelle erstellt haben, können Sie Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1f016-214">Since you created the table, you can make changes to it.</span></span>

    <span data-ttu-id="1f016-215">Sorgen Sie dafür, dass die Firewall aktiviert ist, da das Ausschalten ein Sicherheitsrisiko darstellen könnte.</span><span class="sxs-lookup"><span data-stu-id="1f016-215">Keep your firewall turned on, as turning it off could create a security risk.</span></span>

    <span data-ttu-id="1f016-216">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-216">**Better:**</span></span>

    <span data-ttu-id="1f016-217">Da Sie die Tabelle erstellt haben, können Sie Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1f016-217">Because you created the table, you can make changes to it.</span></span>

    <span data-ttu-id="1f016-218">Sorgen Sie dafür, dass die Firewall aktiviert ist, da das Ausschalten ein Sicherheitsrisiko darstellen könnte.</span><span class="sxs-lookup"><span data-stu-id="1f016-218">Keep your firewall turned on, because turning it off could create a security risk.</span></span>

-   <span data-ttu-id="1f016-219">Lassen Sie unnötige Wörter aus – verwenden Sie nicht zwei oder drei Wörter, wenn eine solche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f016-219">Omit needless words—don't use two or three words when one will do.</span></span>

    <span data-ttu-id="1f016-220">**Ausführliche**</span><span class="sxs-lookup"><span data-stu-id="1f016-220">**Verbose:**</span></span>

    <span data-ttu-id="1f016-221">Führen Sie die folgenden Schritte aus, um Ihr Kennwort zu ändern:</span><span class="sxs-lookup"><span data-stu-id="1f016-221">Follow these steps in order to change your password:</span></span>

    <span data-ttu-id="1f016-222">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-222">**Better:**</span></span>

    <span data-ttu-id="1f016-223">So ändern Sie Ihr Kennwort:</span><span class="sxs-lookup"><span data-stu-id="1f016-223">To change your password:</span></span>

-   <span data-ttu-id="1f016-224">Vermeiden Sie unnötige adversb.</span><span class="sxs-lookup"><span data-stu-id="1f016-224">Avoid unnecessary adverbs.</span></span>

    <span data-ttu-id="1f016-225">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="1f016-225">**Incorrect:**</span></span>

    <span data-ttu-id="1f016-226">Es ist nicht schrecklich schwierig, Ihr Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f016-226">It isn't terribly hard to change your password.</span></span>

    <span data-ttu-id="1f016-227">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-227">**Correct:**</span></span>

    <span data-ttu-id="1f016-228">Es ist nicht schwierig, Ihr Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f016-228">It isn't hard to change your password.</span></span>

-   <span data-ttu-id="1f016-229">Wählen Sie einzelne Wort Verben für Verben mit mehreren Wörtern aus.</span><span class="sxs-lookup"><span data-stu-id="1f016-229">Choose single-word verbs over multi-word verbs.</span></span>

    <span data-ttu-id="1f016-230">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-230">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-231">Wenn Sie den Computer sperren,...</span><span class="sxs-lookup"><span data-stu-id="1f016-231">When you lock down your computer, ...</span></span>

    <span data-ttu-id="1f016-232">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-232">**Better:**</span></span>

    <span data-ttu-id="1f016-233">Wenn Sie den Computer sperren,...</span><span class="sxs-lookup"><span data-stu-id="1f016-233">When you lock your computer, ...</span></span>

-   <span data-ttu-id="1f016-234">Konvertieren Sie Verben nicht in Nomen und Nomen in Verben.</span><span class="sxs-lookup"><span data-stu-id="1f016-234">Don't convert verbs to nouns and nouns to verbs.</span></span>

    <span data-ttu-id="1f016-235">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="1f016-235">**Incorrect:**</span></span>

    <span data-ttu-id="1f016-236">Um den Computer mit einem Kennwort zu schützen...</span><span class="sxs-lookup"><span data-stu-id="1f016-236">To password-protect your computer...</span></span>

    <span data-ttu-id="1f016-237">Zum Herstellen der Konnektivität...</span><span class="sxs-lookup"><span data-stu-id="1f016-237">To establish connectivity...</span></span>

    <span data-ttu-id="1f016-238">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-238">**Correct:**</span></span>

    <span data-ttu-id="1f016-239">So schützen Sie Ihren Computer mit einem Kennwort...</span><span class="sxs-lookup"><span data-stu-id="1f016-239">To protect your computer with a password...</span></span>

    <span data-ttu-id="1f016-240">Verbindung wird hergestellt...</span><span class="sxs-lookup"><span data-stu-id="1f016-240">To connect...</span></span>

### <a name="be-consistent"></a><span data-ttu-id="1f016-241">Einheitlich sein</span><span class="sxs-lookup"><span data-stu-id="1f016-241">Be consistent</span></span>

-   <span data-ttu-id="1f016-242">Konsistente Terminologie fördert das Erlernen von Kenntnissen und ein besseres Verständnis der technischen Konzepte.</span><span class="sxs-lookup"><span data-stu-id="1f016-242">Consistent terminology promotes learning and a better understanding of technical concepts.</span></span> <span data-ttu-id="1f016-243">Die Inkonsistenz zwingt Benutzer, herauszufinden, ob verschiedene Wörter und Aktionen dasselbe Ergebnis bedeuten.</span><span class="sxs-lookup"><span data-stu-id="1f016-243">Inconsistency forces users to figure out whether different words and actions mean the same thing.</span></span>

    <span data-ttu-id="1f016-244">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="1f016-244">Examples:</span></span>

    <span data-ttu-id="1f016-245">umschalten, Umschalten</span><span class="sxs-lookup"><span data-stu-id="1f016-245">switch, toggle</span></span>

    <span data-ttu-id="1f016-246">starten, ausführen, starten, starten, ausführen</span><span class="sxs-lookup"><span data-stu-id="1f016-246">start, run, launch, boot, execute</span></span>

    <span data-ttu-id="1f016-247">aktivieren, aktivieren, einschalten</span><span class="sxs-lookup"><span data-stu-id="1f016-247">enable, activate, turn on</span></span>

    <span data-ttu-id="1f016-248">Brennen, kopieren</span><span class="sxs-lookup"><span data-stu-id="1f016-248">burn, copy</span></span>

-   <span data-ttu-id="1f016-249">Konsistente Syntax hilft beim Festlegen der Erwartungen der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="1f016-249">Consistent syntax helps set users' expectations.</span></span> <span data-ttu-id="1f016-250">Nachdem diese Erwartungen festgelegt wurden, können Benutzer Text schneller analysieren, der eine konsistente Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f016-250">Once these expectations are set, users can more quickly parse text that uses consistent syntax.</span></span> <span data-ttu-id="1f016-251">Wenn z. b. Anweisungen immer im imperativen Format geschrieben werden, lernen Benutzer, dass Sie sich auf imperative Sätze achten müssen.</span><span class="sxs-lookup"><span data-stu-id="1f016-251">For example, if instructions are always written in the imperative form, users will learn to pay closer attention to imperative sentences.</span></span>

### <a name="contractions"></a><span data-ttu-id="1f016-252">Kontraktionen</span><span class="sxs-lookup"><span data-stu-id="1f016-252">Contractions</span></span>

-   <span data-ttu-id="1f016-253">Kontra KTIONEN verleihen einen kürzeren, Auslassungs Zeichen-und besser konvergenten Rhythmus beim Schreiben.</span><span class="sxs-lookup"><span data-stu-id="1f016-253">Contractions lend a shorter, snappier, more conversational rhythm to writing.</span></span> <span data-ttu-id="1f016-254">Verwenden Sie diese nach Bedarf und im Kontext.</span><span class="sxs-lookup"><span data-stu-id="1f016-254">Use them as appropriate and in context.</span></span> <span data-ttu-id="1f016-255">Verwenden Sie keine gegen übereinstigkeiten mit Produktnamen oder anderen richtigen Substantiven.</span><span class="sxs-lookup"><span data-stu-id="1f016-255">Don't use contractions with product names or other proper nouns.</span></span>

### <a name="colloquialisms-idioms-and-slang"></a><span data-ttu-id="1f016-256">Colloquialismen, Idioms und slang</span><span class="sxs-lookup"><span data-stu-id="1f016-256">Colloquialisms, idioms, and slang</span></span>

-   <span data-ttu-id="1f016-257">Verwenden Sie in besonderen Situationen, wie z. b. Produkt Fahrten, Einrichtungs Bildschirme oder Inhalt, der nicht lokalisiert werden soll, die Verwendung von Umgangs-oder-slang.</span><span class="sxs-lookup"><span data-stu-id="1f016-257">Consider using colloquialisms or slang only in special situations, such as product tours, setup screens, or content that won't be localized.</span></span> <span data-ttu-id="1f016-258">In den letzten Studien wurde gezeigt, dass die Benutzer das unerwartete Wort oder den vertrauten Ausdruck genießen.</span><span class="sxs-lookup"><span data-stu-id="1f016-258">Recent studies have shown that users enjoy the unexpected word or familiar phrase.</span></span> <span data-ttu-id="1f016-259">Beachten Sie, dass die Verwendung von Umgangs-und slang möglicherweise schwierig und kostspielig ist, um effektiv zu übersetzen, sodass eine solche Sprache am besten mit Bedacht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1f016-259">Bear in mind that using colloquialisms and slang can be difficult and costly to translate effectively, so such language is best used judiciously.</span></span>

    <span data-ttu-id="1f016-260">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="1f016-260">**Examples:**</span></span>

    <span data-ttu-id="1f016-261">Auf der anderen Seite gibt es jedoch bestimmte Werte in der Registrierung, die nicht geändert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="1f016-261">On the other hand, there are certain values in the registry that shouldn't be changed.</span></span>

    <span data-ttu-id="1f016-262">Mit SDSL ist die Linie für die Verwendung durch den Internet reserviert, sodass Sie im Internet keine gestürzten Verkehrsbehinderungen durchführen können, wie dies bei einem Kabeldienst der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-262">With SDSL, the line is dedicated to your Internet use, so you won't experience rush-hour traffic jams on the Internet, as you might with cable service.</span></span>

### <a name="person"></a><span data-ttu-id="1f016-263">Person</span><span class="sxs-lookup"><span data-stu-id="1f016-263">Person</span></span>

-   <span data-ttu-id="1f016-264">**Wenden Sie sich direkt oder indirekt an den Benutzer.**</span><span class="sxs-lookup"><span data-stu-id="1f016-264">**Address the user as you, directly or indirectly.**</span></span>
-   <span data-ttu-id="1f016-265">**Verwenden Sie die zweite Person (Sie, ihre), um den Benutzern mitzuteilen, was zu tun ist.**</span><span class="sxs-lookup"><span data-stu-id="1f016-265">**Use the second person (you, your) to tell users what to do.**</span></span> <span data-ttu-id="1f016-266">Häufig wird die zweite Person impliziert.</span><span class="sxs-lookup"><span data-stu-id="1f016-266">Often the second person is implied.</span></span>

    <span data-ttu-id="1f016-267">**Beispiele:**</span><span class="sxs-lookup"><span data-stu-id="1f016-267">**Examples:**</span></span>

    <span data-ttu-id="1f016-268">Wählen Sie die Bilder aus, die Sie drucken möchten.</span><span class="sxs-lookup"><span data-stu-id="1f016-268">Choose the pictures you want to print.</span></span>

    <span data-ttu-id="1f016-269">Wählen Sie ein Konto.</span><span class="sxs-lookup"><span data-stu-id="1f016-269">Choose an account.</span></span> <span data-ttu-id="1f016-270">impliziert</span><span class="sxs-lookup"><span data-stu-id="1f016-270">(implied)</span></span>

-   <span data-ttu-id="1f016-271">**Verwenden Sie die erste Person (I, me, my), damit Benutzer dem Programm mitteilen können, was zu tun ist.**</span><span class="sxs-lookup"><span data-stu-id="1f016-271">**Use the first person (I, me, my) to let users tell the program what to do.**</span></span>

    <span data-ttu-id="1f016-272">**Beispiel:**</span><span class="sxs-lookup"><span data-stu-id="1f016-272">**Example:**</span></span>

    <span data-ttu-id="1f016-273">Drucken Sie die Fotos auf meiner Kamera.</span><span class="sxs-lookup"><span data-stu-id="1f016-273">Print the photos on my camera.</span></span>

-   <span data-ttu-id="1f016-274">**Verwenden Sie wir mit Bedacht.**</span><span class="sxs-lookup"><span data-stu-id="1f016-274">**Use we judiciously.**</span></span> <span data-ttu-id="1f016-275">Der Plural der ersten Person kann eine gewaltige Unternehmens Präsenz vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="1f016-275">The first-person plural can suggest a daunting corporate presence.</span></span> <span data-ttu-id="1f016-276">Es ist jedoch besser, den Namen Ihrer Anwendung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f016-276">However, it can be preferable to using the name of your application.</span></span> <span data-ttu-id="1f016-277">Wir empfehlen Ihnen, anstelle der empfohlenen Verwendung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f016-277">Use we recommend rather than it is recommended.</span></span>
-   <span data-ttu-id="1f016-278">**Vermeiden Sie Verweise von Dritt Personen (Benutzer)** , da Sie einen formelleren, weniger persönlichen Ton erstellen.</span><span class="sxs-lookup"><span data-stu-id="1f016-278">**Avoid third-person references (the user)** because they create a more formal, less personal tone.</span></span>

### <a name="voice"></a><span data-ttu-id="1f016-279">Sprache</span><span class="sxs-lookup"><span data-stu-id="1f016-279">Voice</span></span>

-   <span data-ttu-id="1f016-280">**Verwenden Sie die aktive Stimme,** mit der die Person oder das, das die Aktion durchführen, hervorgehoben wird</span><span class="sxs-lookup"><span data-stu-id="1f016-280">**Use the active voice,** which emphasizes the person or thing doing the action.</span></span> <span data-ttu-id="1f016-281">Es ist direkter und persönlicher als die passive Stimme, was verwirrend oder audioformal sein kann.</span><span class="sxs-lookup"><span data-stu-id="1f016-281">It is more direct and personal than the passive voice, which can be confusing or sound formal.</span></span>

    <span data-ttu-id="1f016-282">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-282">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-283">Symbole können nach Namen in alphabetischer Reihenfolge angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-283">Icons can be arranged by name in alphabetical order.</span></span>

    <span data-ttu-id="1f016-284">Wenn ein persönlicher digitaler Assistent (PDA) oder Laptop angeschlossen ist...</span><span class="sxs-lookup"><span data-stu-id="1f016-284">When a Personal Digital Assistant (PDA) or laptop is plugged in...</span></span>

    <span data-ttu-id="1f016-285">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-285">**Better:**</span></span>

    <span data-ttu-id="1f016-286">Sie können Symbole in alphabetischer Reihenfolge nach dem Symbolnamen anordnen.</span><span class="sxs-lookup"><span data-stu-id="1f016-286">You can arrange icons in alphabetical order by the icon name.</span></span>

    <span data-ttu-id="1f016-287">Wenn Sie einen beliebigen persönlichen Digital Assistant (PDA) oder Laptop anschließen...</span><span class="sxs-lookup"><span data-stu-id="1f016-287">When you plug in any Personal Digital Assistant (PDA) or laptop...</span></span>

-   <span data-ttu-id="1f016-288">Verwenden Sie die passive Stimme nur, um eine verfassen-oder unschöne Konstruktion zu vermeiden. Wenn die Aktion nicht der hoch ist, liegt der Schwerpunkt auf dem Satz. Wenn der Betreff unbekannt ist. oder in Fehlermeldungen, wenn der Benutzer den Betreff hat und wahrscheinlich für den Fehler verantwortlich ist, wenn die aktive Stimme verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1f016-288">Use the passive voice only to avoid a wordy or awkward construction; when the action rather than the doer is the focus of the sentence; when the subject is unknown; or in error messages, when the user is the subject and might feel blamed for the error if the active voice were used.</span></span>

    <span data-ttu-id="1f016-289">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-289">**Correct:**</span></span>

    <span data-ttu-id="1f016-290">Das neue Symbol sollte in der oberen linken Ecke angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-290">The new icon should appear in the upper-left corner.</span></span>

    <span data-ttu-id="1f016-291">Updates müssen heruntergeladen und installiert werden, damit Sie funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="1f016-291">Updates must be downloaded and installed before they can work.</span></span>

-   <span data-ttu-id="1f016-292">**Ausdrucks Anweisungen in der positiven Form** und betonen, was Benutzer tun können, anstatt Sie zu überschreiten.</span><span class="sxs-lookup"><span data-stu-id="1f016-292">**Phrase statements in the positive form**, and emphasize what users can accomplish, rather than what they can't.</span></span>

### <a name="attitude-toward-the-user"></a><span data-ttu-id="1f016-293">Haltung zum Benutzer</span><span class="sxs-lookup"><span data-stu-id="1f016-293">Attitude toward the user</span></span>

-   <span data-ttu-id="1f016-294">**Seien Sie höflich, unterstützend und ermutigend.**</span><span class="sxs-lookup"><span data-stu-id="1f016-294">**Be polite, supportive, and encouraging.**</span></span> <span data-ttu-id="1f016-295">Der Benutzer sollte sich niemals an einen oder anderen Benutzer fühlen.</span><span class="sxs-lookup"><span data-stu-id="1f016-295">The user should never feel condescended to, blamed, or intimidated.</span></span>

    <span data-ttu-id="1f016-296">**Annehmbar:**</span><span class="sxs-lookup"><span data-stu-id="1f016-296">**Acceptable:**</span></span>

    <span data-ttu-id="1f016-297">Das neue Text Dokument kann nicht gelöscht werden: der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="1f016-297">Cannot delete New Text Document: Access is denied.</span></span>

    <span data-ttu-id="1f016-298">**Besserer**</span><span class="sxs-lookup"><span data-stu-id="1f016-298">**Better:**</span></span>

    <span data-ttu-id="1f016-299">Diese Datei ist geschützt und kann ohne spezielle Berechtigung nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-299">This file is protected and cannot be deleted without specific permission.</span></span>

-   <span data-ttu-id="1f016-300">**Erreichen Sie das richtige Gleichgewicht: seien Sie für den Benutzer so, dass er nicht zu intim oder zu Geschäfts ähnlich ist.**</span><span class="sxs-lookup"><span data-stu-id="1f016-300">**Strike the right balance: be warm toward the user without being too intimate or too business-like.**</span></span> <span data-ttu-id="1f016-301">Stellen Sie sich vor, dass Sie einem Freund helfen, das Produkt zum ersten Mal zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f016-301">Imagine that you are helping a friend use the product for the first time.</span></span> <span data-ttu-id="1f016-302">Diese Person ist nicht der beste Freund, sondern ein Nachbar oder Familienfreund.</span><span class="sxs-lookup"><span data-stu-id="1f016-302">This person is not your best friend or significant other, but instead, a neighbor or family friend.</span></span> <span data-ttu-id="1f016-303">Benutzer sollten sich bei der Verwendung des Programms als gut ansehen, aber die Sprache sollte nicht anmaßend oder zu vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="1f016-303">Users should feel comfortable and at home when using your program, but the language should not feel presumptuous or too familiar.</span></span>
-   <span data-ttu-id="1f016-304">**Beschränken Sie in Situationen, in denen der Benutzer nicht beeinträchtigt wird,** z. b.:</span><span class="sxs-lookup"><span data-stu-id="1f016-304">**Limit please to situations that inconvenience the user in some way,** such as:</span></span>

    -   <span data-ttu-id="1f016-305">Der Benutzer wird aufgefordert, etwas unpraktisch zu machen, z. b. das warten, das Wiederholen einer Aufgabe oder das Aktualisieren eines Programms.</span><span class="sxs-lookup"><span data-stu-id="1f016-305">The user is asked to do something inconvenient, such as waiting, repeating a task or updating a program.</span></span>

        <span data-ttu-id="1f016-306">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-306">**Correct:**</span></span>

        <span data-ttu-id="1f016-307">Bitte warten Sie, während die Dateien von Windows auf Ihren Computer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f016-307">Please wait while Windows copies the files to your computer.</span></span>

    -   <span data-ttu-id="1f016-308">Der Benutzer kann eine Aufgabe aufgrund fehlender Features, Entwurfs Fehler oder Programmfehler nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f016-308">The user can't complete a task because of a missing feature, design flaw, or program bug.</span></span>

        <span data-ttu-id="1f016-309">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-309">**Correct:**</span></span>

        <span data-ttu-id="1f016-310">Das Speichern mit dem angegebenen Format ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="1f016-310">Unable to save using the specified format.</span></span> <span data-ttu-id="1f016-311">Wählen Sie ein anderes Format aus.</span><span class="sxs-lookup"><span data-stu-id="1f016-311">Please select another format.</span></span>

    -   <span data-ttu-id="1f016-312">Der Benutzer hat seine Möglichkeit verlassen, um hilfreich zu sein, da er an einem Kundenfeedback Programm teilnimmt oder einen Fehlerbericht eingibt.</span><span class="sxs-lookup"><span data-stu-id="1f016-312">The user has gone out of his or her way to be helpful, as by participating in a customer feedback program or filing a bug report.</span></span>

        <span data-ttu-id="1f016-313">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-313">**Correct:**</span></span>

        <span data-ttu-id="1f016-314">Um die Fabrikam-Sicherung zu verbessern, nehmen Sie am Kundenfeedback Programm von Fabrikam Teil.</span><span class="sxs-lookup"><span data-stu-id="1f016-314">To improve the Fabrikam Backup experience, please participate in the Fabrikam customer feedback program.</span></span>

    <span data-ttu-id="1f016-315">Sie sollten auch immer dann verwenden, wenn ihre Abwesenheit als Curt angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="1f016-315">You should also use please whenever its absence would be considered curt.</span></span>

    ![<span data-ttu-id="1f016-316">Screenshot der Richtungen, die mit "bitte" beginnen</span><span class="sxs-lookup"><span data-stu-id="1f016-316">screen shot of directions beginning with please</span></span> ](images/text-style-tone-image1.png)

    <span data-ttu-id="1f016-317">In diesem Beispiel sind die Inline Fehlermeldungen ohne bitte "Curt".</span><span class="sxs-lookup"><span data-stu-id="1f016-317">In this example, the inline error messages would be curt without please.</span></span>

-   <span data-ttu-id="1f016-318">**Verwenden Sie leider nur Fehlermeldungen, die zu schwerwiegenden Problemen für den Benutzer führen** (z. b. Datenverlust, der Benutzer kann den Computer nicht weiter verwenden, oder der Benutzer muss von einem technischen Vertreter unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="1f016-318">**Use sorry only in error messages that result in serious problems for the user** (for example, data loss, the user can't continue to use the computer, or the user must get help from a technical representative).</span></span> <span data-ttu-id="1f016-319">Entschuldigen Sie nicht, wenn das Problem während der normalen Funktionsweise des Programms aufgetreten ist (z. b. wenn der Benutzer auf eine Netzwerkverbindung warten muss).</span><span class="sxs-lookup"><span data-stu-id="1f016-319">Don't apologize if the issue occurred during the normal functioning of the program (for example, if the user needs to wait for a network connection to be found).</span></span>

    <span data-ttu-id="1f016-320">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-320">**Correct:**</span></span>

    <span data-ttu-id="1f016-321">Leider hat die Fabrikam-Sicherung ein nicht BEHEB bares Problem festgestellt und wurde heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="1f016-321">We're sorry, but Fabrikam Backup detected an unrecoverable problem and was shut down.</span></span>

### <a name="sentence-structure-and-length"></a><span data-ttu-id="1f016-322">Satzstruktur und-Länge</span><span class="sxs-lookup"><span data-stu-id="1f016-322">Sentence structure and length</span></span>

-   <span data-ttu-id="1f016-323">Da Benutzer häufig Text scannen, **machen Sie jede Wort Anzahl.**</span><span class="sxs-lookup"><span data-stu-id="1f016-323">Because users often scan text, **make every word count.**</span></span> <span data-ttu-id="1f016-324">Einfache, präzise Sätze (und Absätze) sparen nicht nur Speicherplatz auf dem Bildschirm, sondern sind das effektivste Mittel, um zu vermitteln, dass eine Idee oder eine Aktion wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-324">Simple, concise sentences (and paragraphs) not only save space on the screen but are the most effective means of conveying that an idea or action is important.</span></span> <span data-ttu-id="1f016-325">Verwenden Sie Ihre Best-Urteils – legen Sie Sätze eng, aber nicht so streng, dass der Ton abrupt und unschädlich erscheint.</span><span class="sxs-lookup"><span data-stu-id="1f016-325">Use your best judgment—make sentences tight, but not so tight that the tone seems abrupt and unfriendly.</span></span>
-   <span data-ttu-id="1f016-326">**Vermeiden Sie eine Wiederholung.**</span><span class="sxs-lookup"><span data-stu-id="1f016-326">**Avoid repetition.**</span></span> <span data-ttu-id="1f016-327">Überprüfen Sie jedes Fenster, und vermeiden Sie doppelte Wörter und Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1f016-327">Review each window and eliminate duplicate words and statements.</span></span> <span data-ttu-id="1f016-328">Vermeiden Sie einen wichtigen Text – bei Bedarf explizit – Sie sind aber nicht redundant, und erläutern Sie nichts, was Sie sagen müssen.</span><span class="sxs-lookup"><span data-stu-id="1f016-328">Don't avoid important text—be explicit whenever necessary—but don't be redundant and don't explain things that go without saying.</span></span>
-   <span data-ttu-id="1f016-329">**Verwenden Sie gegebenenfalls Satzfragmente.**</span><span class="sxs-lookup"><span data-stu-id="1f016-329">**Use sentence fragments if appropriate.**</span></span> <span data-ttu-id="1f016-330">Satzfragmente sind kurz und punssig – und wenn Sie in der Regel das abgefragende Formular verwenden, sind Sie eine gute Methode, um den Benutzer direkt einzubinden.</span><span class="sxs-lookup"><span data-stu-id="1f016-330">Sentence fragments are short and punchy—and, as they typically take the interrogative form, they are a good way of directly engaging the user.</span></span>

    <span data-ttu-id="1f016-331">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-331">**Correct:**</span></span>

    <span data-ttu-id="1f016-332">Werden die Änderungen an "meine Fotos" gespeichert?</span><span class="sxs-lookup"><span data-stu-id="1f016-332">Save changes to "My Photos"?</span></span>

    <span data-ttu-id="1f016-333">Haben Sie jemals eine Datei gespeichert und dann nicht daran gespeichert, wo Sie Sie gespeichert haben?</span><span class="sxs-lookup"><span data-stu-id="1f016-333">Ever saved a file and then not remembered where you saved it?</span></span>

-   <span data-ttu-id="1f016-334">**Beginnen Sie mit** der Verwendung von-Sätzen (und, aber oder), wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1f016-334">**Start sentences with conjunctions** (and, but, or) if you need to.</span></span>
-   <span data-ttu-id="1f016-335">**Ersetzen Sie Listen und Tabellen in komplexen Sätzen.**</span><span class="sxs-lookup"><span data-stu-id="1f016-335">**Substitute lists and tables for complex sentences.**</span></span> <span data-ttu-id="1f016-336">Listen (ob nummeriert oder aufzählig) und Tabellen sind übersichtlicher und leichter zu scannen.</span><span class="sxs-lookup"><span data-stu-id="1f016-336">Lists (whether numbered or bulleted) and tables are clearer and easier to scan.</span></span>
-   <span data-ttu-id="1f016-337">**Verwenden paralleler Grammatiken.**</span><span class="sxs-lookup"><span data-stu-id="1f016-337">**Use parallel grammatical constructions.**</span></span> <span data-ttu-id="1f016-338">Parallelität erfordert, dass Wörter und Ausdrücke, die dieselbe Funktion aufweisen, dieselbe Form aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1f016-338">Parallelism requires that words and phrases that have the same function have the same form.</span></span> <span data-ttu-id="1f016-339">Verwenden Sie die parallele Sprache immer dann, wenn Sie Ideen von gleicher Gewichtung und Benutzeroberflächen Elemente, die parallel in der Funktion sind (z. b. Überschriften, Bezeichnungen, Listen oder Seitentitel), Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="1f016-339">Use parallel language whenever you express ideas of equal weight, and for UI elements that are parallel in function (such as headings, labels, lists, or page titles).</span></span>

    <span data-ttu-id="1f016-340">**Richtig:**</span><span class="sxs-lookup"><span data-stu-id="1f016-340">**Correct:**</span></span>

    <span data-ttu-id="1f016-341">Lauschen</span><span class="sxs-lookup"><span data-stu-id="1f016-341">Listen</span></span>

    <span data-ttu-id="1f016-342">Überwachen</span><span class="sxs-lookup"><span data-stu-id="1f016-342">Watch</span></span>

    <span data-ttu-id="1f016-343">Teilen</span><span class="sxs-lookup"><span data-stu-id="1f016-343">Share</span></span>

    <span data-ttu-id="1f016-344">Collect</span><span class="sxs-lookup"><span data-stu-id="1f016-344">Collect</span></span>

    <span data-ttu-id="1f016-345">Diese Elemente sind parallel, da es sich um ein einzelnes Wort, Imperatives Verben handelt.</span><span class="sxs-lookup"><span data-stu-id="1f016-345">These items are parallel because they are all single-word, imperative verbs.</span></span>

    <span data-ttu-id="1f016-346">**Falsch:**</span><span class="sxs-lookup"><span data-stu-id="1f016-346">**Incorrect:**</span></span>

    <span data-ttu-id="1f016-347">Musik</span><span class="sxs-lookup"><span data-stu-id="1f016-347">Music</span></span>

    <span data-ttu-id="1f016-348">Video</span><span class="sxs-lookup"><span data-stu-id="1f016-348">Video</span></span>

    <span data-ttu-id="1f016-349">Teilen</span><span class="sxs-lookup"><span data-stu-id="1f016-349">Share</span></span>

    <span data-ttu-id="1f016-350">Lauschen</span><span class="sxs-lookup"><span data-stu-id="1f016-350">Listen</span></span>

    <span data-ttu-id="1f016-351">Diese Elemente sind nicht parallel, da Musik und Video Nomen sind, aber freigeben und lauschen sind Verben.</span><span class="sxs-lookup"><span data-stu-id="1f016-351">These items are not parallel because Music and Video are nouns, but Share and Listen are verbs.</span></span>

 

 