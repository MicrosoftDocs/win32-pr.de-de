---
title: Sicherheitsüberlegungen für Hilfstechnologien
description: Hilfstechnologien sind Anwendungen, die auf dem Windows-Desktop ausgeführt werden und Benutzer der Benutzerfreundlichkeit bei der Interaktion mit dem Betriebssystem und anderen Anwendungen auf dem Computer unterstützen, einschließlich Anwendungen in der neuen Windows-Benutzeroberfläche.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- UIAccess-Attribut
- UI-Automatisierung, UIAccess-Attribut
- Sicherheit, UIAccess-Attribut
- requestedExecutionLevel-Tag
- Benutzeroberflächenautomatisierungs-Tag (requestedExecutionLevel)
- Benutzeroberflächenautomatisierungs, Sicherheitsüberlegungen
- Benutzeroberflächenautomatisierungs, Manifest-Dateien
- Manifest-Dateien
- Benutzerkontensteuerung
- Sicherheit, Benutzerkontensteuerung
- Sicherheit, Manifest-Dateien
- Sicherheit, requestedExecutionLevel-Tag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106340292"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="67be7-115">Sicherheitsüberlegungen für Hilfstechnologien</span><span class="sxs-lookup"><span data-stu-id="67be7-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="67be7-116">Hilfstechnologien sind Anwendungen, die auf dem Windows-Desktop ausgeführt werden und Barrierefreiheits Benutzer bei der Interaktion mit dem Betriebssystem und anderen Anwendungen auf dem Computer unterstützen, einschließlich der Anwendungen in der neuen Windows-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="67be7-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="67be7-117">Hilfstechnologieanwendungen arbeiten durch Abrufen von Informationen vom Betriebssystem und anderen Anwendungen und anschließendes darstellen der Informationen auf eine Weise, auf die der Benutzer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="67be7-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="67be7-118">Eine hilfstechnologieanwendung kann das Betriebssystem und andere Anwendungen auch Programm gesteuert auf der Grundlage der Benutzereingaben steuern.</span><span class="sxs-lookup"><span data-stu-id="67be7-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="67be7-119">Die Art von Hilfstechnologieanwendungen erfordert, dass Sie prozessübergreifende Grenzen überschreiten und Zugriff auf Prozesse haben, die mit einer höheren Integritäts Ebene (IL) als sich selbst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67be7-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="67be7-120">(Eine hilfstechnologieanwendung wird mit mittlerer Il ausgeführt.) Wenn der Benutzer z. b. versucht, eine Aufgabe auszuführen, für die Administratorrechte erforderlich sind, wird in Windows ein Dialogfeld angezeigt, in dem der Benutzer zum Fortfahren aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="67be7-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="67be7-121">Dieses Dialogfeld wird mit einer höheren Integritäts Stufe ausgeführt, um es vor Prozess übergreifender Kommunikation zu schützen, damit Schadsoftware keine Benutzereingaben simulieren kann.</span><span class="sxs-lookup"><span data-stu-id="67be7-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="67be7-122">Auf ähnliche Weise wird der Desktop Anmeldebildschirm mit einer höheren Integritäts Stufe ausgeführt, um zu verhindern, dass andere Prozesse darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="67be7-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="67be7-123">Hilfstechnologieanwendungen benötigen in der Regel Zugriff auf die Benutzeroberflächen Elemente des geschützten Systems oder auf andere Prozesse, die möglicherweise auf einer höheren Berechtigungsstufe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67be7-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="67be7-124">Daher müssen Hilfstechnologieanwendungen vom System als vertrauenswürdig eingestuft werden und müssen mit besonderen Berechtigungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67be7-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="67be7-125">Um Zugriff auf höhere Il-Prozesse zu erhalten, muss eine hilfstechnologieanwendung das UIAccess-Flag im Manifest der Anwendung festlegen und von einem Benutzer mit Administratorrechten gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="67be7-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="67be7-126">Zugriffsberechtigungen werden wie folgt eingeschränkt:</span><span class="sxs-lookup"><span data-stu-id="67be7-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="67be7-127">Eine Anwendung, die keinen UIAccess im Manifest hat, beginnt mit mittlerer Il und kann nicht auf die Benutzeroberfläche mit erhöhten Rechten ("Mittel +" Il-Prozess) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="67be7-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="67be7-128">Eine Anwendung, die über UIAccess im Manifest verfügt und von einem Benutzer gestartet wird, der nicht der Gruppe "Administratoren" angehört, beginnt mit "Mittel +" und kann nicht auf die Benutzeroberfläche mit erhöhten Rechten zugreifen (es wird keine "hohe" Il ausgeführt, wie z. b. apps, die über einen **Rechtsklick > als Administrator ausgeführt** werden).</span><span class="sxs-lookup"><span data-stu-id="67be7-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="67be7-129">Eine Anwendung verfügt über Zugriff auf die Benutzeroberfläche und wird von einem Administrator gestartet, der als "High" Il startet und auf die Benutzeroberfläche mit erhöhten Rechten zugreifen kann, da Sie die gleiche Il hat</span><span class="sxs-lookup"><span data-stu-id="67be7-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="67be7-130">UIAccess reicht nicht aus, damit ein Prozess über die Il-Grenze nach oben verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="67be7-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="67be7-131">Zusätzlich zum Zugriff auf höhere Il-Prozesse kann eine hilfstechnologieanwendung mit diesen Berechtigungen jederzeit in der z-Reihenfolge als oberste Anwendung ausgeführt werden. Dies bedeutet, dass eine hilfstechnologieanwendung sichtbar und verfügbar sein kann, wenn der Benutzer Sie benötigt.</span><span class="sxs-lookup"><span data-stu-id="67be7-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="67be7-132">Keines der zuvor aufgeführten Szenarien bietet Zugriff auf die Benutzeroberfläche, die unter der System-Il ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67be7-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="67be7-133">Dies ist nur möglich, wenn der Prozess im Desktop der Benutzerkontensteuerung (User Account Control, UAC) unter System (und System IL) gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="67be7-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="67be7-134">In diesem Fall hat das Festlegen von UIAccess keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="67be7-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="67be7-135">UIAccess-Anforderungen für Hilfstechnologieanwendungen</span><span class="sxs-lookup"><span data-stu-id="67be7-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="67be7-136">Eine hilfstechnologieanwendung ist eine Windows-Desktop Anwendung, die mit anderen Prozessen interagiert, die auf dem Desktop und in der neuen Windows-Benutzeroberfläche ausgeführt werden, um Informationen aus dem System und den Anwendungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="67be7-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="67be7-137">Die hilfstechnologieanwendung kann die Informationen dann für Barrierefreiheits Benutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="67be7-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="67be7-138">Eine hilfstechnologieanwendung erhält Zugriff auf andere Prozesse, indem das UIAccess-Flag im Anwendungs Manifest festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="67be7-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="67be7-139">Um das UIAccess-Flag zu verwenden, muss eine hilfstechnologieanwendung die folgenden Anforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="67be7-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="67be7-140">Erfordert, dass Informationen für ein Barrierefreiheits Szenario angezeigt, mit einer anderen Anwendung interagiert oder wieder angezeigt werden, um Informationen für ein Barrierefreiheits Szenario bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="67be7-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="67be7-141">Erfordert die Ausführung als oberstes Fenster, um diese Informationen zu erhalten oder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="67be7-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="67be7-142">Um UIAccess zu verwenden, muss eine hilfstechnologieanwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="67be7-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="67be7-143">Sie müssen mit einem Zertifikat signiert werden, um mit Anwendungen zu interagieren, die auf einer höheren Berechtigungsstufe ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="67be7-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="67be7-144">Wird vom System als vertrauenswürdig eingestuft.</span><span class="sxs-lookup"><span data-stu-id="67be7-144">Be trusted by the system.</span></span> <span data-ttu-id="67be7-145">Die Anwendung muss an einem sicheren Speicherort installiert sein, der eine Eingabeaufforderung für die Benutzerkontensteuerung (User Account Control, UAC) erfordert.</span><span class="sxs-lookup"><span data-stu-id="67be7-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="67be7-146">Beispielsweise der Ordner "Programme".</span><span class="sxs-lookup"><span data-stu-id="67be7-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="67be7-147">Sie sollten mit einer Manifest-Datei erstellt werden, die das UIAccess-Flag enthält.</span><span class="sxs-lookup"><span data-stu-id="67be7-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="67be7-148">UIAccess sollte nicht verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="67be7-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="67be7-149">Anwendungen, bei denen es sich nicht um Hilfstechnologien handelt.</span><span class="sxs-lookup"><span data-stu-id="67be7-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="67be7-150">Von Hilfstechnologieanwendungen, in denen Informationen oder Benutzeroberflächen angezeigt werden, die für das für die Barrierefreiheit relevante Szenario nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="67be7-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="67be7-151">Von Anwendungen, die nur über anderen Anwendungen in der neuen Windows-Benutzeroberfläche angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67be7-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="67be7-152">Anwendungen, die für die neue Windows-Benutzeroberfläche entwickelt wurden, verfügen nicht über UIAccess als verfügbare Option.</span><span class="sxs-lookup"><span data-stu-id="67be7-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="67be7-153">Festlegen von UIAccess in der Anwendungs Manifest-Datei</span><span class="sxs-lookup"><span data-stu-id="67be7-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="67be7-154">Für den Zugriff auf die Benutzeroberfläche des geschützten Systems müssen Anwendungen mit einer Manifestressource erstellt werden, die ein spezielles Attribut in der Manifest-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="67be7-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="67be7-155">Dieses **UIAccess** -Attribut ist im **requestedExecutionLevel** -Tag enthalten, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="67be7-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="67be7-156">Der Wert des **Levels** -Attributs in diesem Code ist nur ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="67be7-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="67be7-157">**UIAccess** ist standardmäßig "false".</span><span class="sxs-lookup"><span data-stu-id="67be7-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="67be7-158">Wenn das Attribut ausgelassen wird oder kein Manifest vorhanden ist, kann die Anwendung keinen Zugriff auf die geschützte Benutzeroberfläche erhalten.</span><span class="sxs-lookup"><span data-stu-id="67be7-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="67be7-159">Weitere Informationen zur Windows-Sicherheit, zum Signieren von Anwendungen und zum Erstellen von Manifesten finden Sie [unter Windows Vista und Windows Server 2008 Developer Story: Anforderungen für die Windows Vista-Anwendungsentwicklung für die Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/aa905330(v=msdn.10)) auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="67be7-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67be7-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67be7-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67be7-161">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="67be7-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 