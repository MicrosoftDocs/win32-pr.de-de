---
title: Sichern und Wiederherstellen von DRM-Lizenzen
description: Sichern und Wiederherstellen von DRM-Lizenzen
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media-Format-SDK, Sichern von DRM-Lizenzen
- Windows Media Format SDK, Wiederherstellen von DRM-Lizenzen
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Windows Media-Format-SDK, Sicherungs Wiederherstellungs Feature
- Windows Media-Format-SDK, Lizenz Verwaltungsdienst
- Windows Media-Format-SDK, Betrugserkennung
- Digital Rights Management (DRM), Sichern von Lizenzen
- DRM (Digital Rights Management), Sichern von Lizenzen
- Digital Rights Management (DRM), Wiederherstellen von Lizenzen
- DRM (Digital Rights Management), Wiederherstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Sicherungs Wiederherstellungs Feature
- DRM (Digital Rights Management), Sicherungs Wiederherstellungs Feature
- Digital Rights Management (DRM), Lizenz Verwaltungsdienst
- DRM (Digital Rights Management), Lizenz Verwaltungsdienst
- Digital Rights Management (DRM), Betrugserkennung
- DRM (Digital Rights Management), Betrugserkennung
- Sichern von DRM-Lizenzen
- Herstellen von DRM-Lizenzen
- Lizenzen, DRM
- Lizenzen, Sichern von DRM
- Lizenzen, Wiederherstellen von DRM
- Sicherungs Wiederherstellungs Feature
- Lizenz Verwaltungsdienst
- Betrugserkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104316652"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="bcc03-130">Sichern und Wiederherstellen von DRM-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="bcc03-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="bcc03-131">Mit dem Feature für die Sicherungs Wiederherstellung können Benutzer [*Lizenzen*](wmformat-glossary.md) auf demselben Computer oder auf anderen Computern sichern und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="bcc03-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="bcc03-132">Diese Funktion ermöglicht es Benutzern, Lizenzen auf einen neuen Computer oder zurück an denselben Computer zu übertragen (z. b. nach dem erneuten Formatieren der Festplatte).</span><span class="sxs-lookup"><span data-stu-id="bcc03-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="bcc03-133">Außerdem können Benutzer geschützte ASF-Dateien auf mehr als einem Computer wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="bcc03-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="bcc03-134">Um die legitime Verwendung einer Lizenz zu fördern, schränkt eine Richtlinie zur Betrugserkennung ein, wie oft eine Lizenz wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="bcc03-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="bcc03-135">Microsoft stellt einen Dienst bereit, mit dem die Anzahl der Computer nachverfolgt wird, auf denen eine Lizenz wieder hergestellt wurde. Wenn ein Grenzwert erreicht wird, kann der Benutzer die Lizenz nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="bcc03-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="bcc03-136">Zulassen oder Deaktivieren der Berechtigung zum Sichern und Wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="bcc03-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="bcc03-137">Die Sicherungs Wiederherstellungs Funktion funktioniert nur für Lizenzen, für die das Sicherungs-und Wiederherstellungs Recht erteilt wurde.</span><span class="sxs-lookup"><span data-stu-id="bcc03-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="bcc03-138">Wenn Inhalts Besitzer oder Lizenz Aussteller diese Funktion nicht wünschen oder wenn Sie Lizenzen ausstellen, die einen sicheren Zustand (z. b. gezählte Vorgänge oder begrenzte Zeit) enthalten, können Sie dieses Recht nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="bcc03-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="bcc03-139">Wenn eine Lizenz nicht wieder hergestellt werden kann, weil ein Benutzer nicht über das Recht verfügt, wird eine [*Schlüssel-ID*](wmformat-glossary.md) an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="bcc03-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="bcc03-140">Der Benutzer sollte mindestens benachrichtigt werden, dass einige Lizenzen nicht gesichert werden konnten, obwohl der Benutzer nicht weiß, auf welche Lizenzen diese Nachricht verweist.</span><span class="sxs-lookup"><span data-stu-id="bcc03-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="bcc03-141">Wenn Sie die Schlüssel-ID für verfügbare geschützte Dateien kennen, können Sie eine stabilere Lösung für die Information des Benutzers entwickeln.</span><span class="sxs-lookup"><span data-stu-id="bcc03-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="bcc03-142">Beispielsweise könnte ein Player für eine Daten Satz Bezeichnung entwickelt werden, die geschützte Lieder im Internet bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bcc03-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="bcc03-143">Diese Lieder und Ihre Schlüssel-IDs können in einer Datenbank nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="bcc03-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="bcc03-144">Wenn einige Lizenzen nicht gesichert werden konnten, könnte die Player Anwendung die Schlüssel-ID verwenden, um die Datenbank nach dem Namen der Lieder abzufragen, und dann den Benutzer darüber informieren, welche Lieder nicht gesichert werden können.</span><span class="sxs-lookup"><span data-stu-id="bcc03-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="bcc03-145">Oder eine Musikbibliothek kann für jeden Benutzer lokal erstellt werden, und die Schlüssel-ID kann verwendet werden, um weitere Informationen darüber abzurufen, welche Lizenzen nicht gesichert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="bcc03-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="bcc03-146">Der Lizenz Verwaltungsdienst</span><span class="sxs-lookup"><span data-stu-id="bcc03-146">The License Management Service</span></span>

<span data-ttu-id="bcc03-147">Wenn die Sicherungs Wiederherstellungs Funktion implementiert ist, verwaltet ein von Microsoft gehosteter Lizenz Verwaltungsdienst die Wiederherstellung von Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="bcc03-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="bcc03-148">Zuerst sichern Benutzerlizenzen in der Anwendung, z. b. durch Auswahl einer Menüoption.</span><span class="sxs-lookup"><span data-stu-id="bcc03-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="bcc03-149">Alle Lizenzen auf dem Computer werden an einem angegebenen Speicherort, z. b. einer Diskette, gesichert.</span><span class="sxs-lookup"><span data-stu-id="bcc03-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="bcc03-150">Anschließend stellen Benutzerlizenzen mithilfe der Anwendung wieder her, indem Sie beispielsweise eine Menüoption auswählen und deren Sicherungs Speicherort angeben.</span><span class="sxs-lookup"><span data-stu-id="bcc03-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="bcc03-151">An diesem Punkt muss der Benutzer mit dem Internet verbunden sein. eine Anforderung von der Anwendung wird an den Lizenz Verwaltungsdienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="bcc03-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="bcc03-152">Wenn der Computer, von dem die Lizenz gesichert wurde, nicht mit dem ursprünglichen Computer identisch ist (oder der ursprüngliche Computer neu formatiert wurde), gibt der Lizenz Verwaltungsdienst eine neue Lizenz für den neuen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="bcc03-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="bcc03-153">Andernfalls wird die Lizenz, die zuvor für diesen Computer ausgestellt wurde, neu ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="bcc03-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="bcc03-154">Da der Lizenz Verwaltungsdienst Informationen vom Benutzer abruft, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der [Microsoft](https://www.microsoft.com/licensing/default)-Website angeben.</span><span class="sxs-lookup"><span data-stu-id="bcc03-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="bcc03-155">Wenn ein Endbenutzer eine Lizenz auf einem anderen Computer wiederherstellt und die Lizenz eine Individualisierung erfordert, muss der Endbenutzer die zu aktualisierenden DRM-Komponenten autorisieren.</span><span class="sxs-lookup"><span data-stu-id="bcc03-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="bcc03-156">Zur Unterstützung dieses Features müssen Sie in der Player Anwendung einen Prozess implementieren.</span><span class="sxs-lookup"><span data-stu-id="bcc03-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="bcc03-157">Erkennen von Betrug</span><span class="sxs-lookup"><span data-stu-id="bcc03-157">Detecting Fraud</span></span>

<span data-ttu-id="bcc03-158">Der Benutzer ist berechtigt, eine Lizenz auf eine begrenzte Anzahl von Zeiten wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bcc03-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="bcc03-159">Jedes Mal, wenn eine Lizenz wieder hergestellt wird, wird Sie vom Lizenz Verwaltungsdienst nachverfolgt, und die Anzahl für diese Lizenz wird um eins erhöht.</span><span class="sxs-lookup"><span data-stu-id="bcc03-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="bcc03-160">Wenn Sie eine Lizenz auf einem Computer wiederherstellen, auf dem die Lizenz zuvor wieder hergestellt wurde (z. b. auf dem Computer, von dem die Lizenz gesichert wurde), wird die Anzahl nicht angehoben.</span><span class="sxs-lookup"><span data-stu-id="bcc03-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="bcc03-161">Ein Computer gilt als anders, wenn er ein neues Betriebssystem aufweist oder das Betriebssystem neu installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="bcc03-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="bcc03-162">In Übereinstimmung mit der Betrugs Erkennungs Richtlinie von Microsoft, wenn eine Lizenz eine bestimmte Anzahl von Wiederholungen wieder hergestellt wurde, empfängt die Anwendung eine URL von den DRM-Komponenten und ist für das Öffnen eines Browsers und das Anzeigen der Webseite zuständig. Dies deutet darauf hin, dass die Lizenzvereinbarung möglicherweise verletzt wurde.</span><span class="sxs-lookup"><span data-stu-id="bcc03-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="bcc03-163">Der Benutzer muss sich an den Lizenz Verteiler wenden, der dann ermitteln muss, ob die Anforderung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="bcc03-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="bcc03-164">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcc03-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bcc03-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bcc03-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcc03-166">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="bcc03-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="bcc03-167">**Sichern und Wiederherstellen von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="bcc03-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




