---
description: Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in der Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installer-Eigenschaften im Windows Installer Paket der Anwendung festlegen.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/30/2021
ms.locfileid: "106372535"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="fa632-103">Konfigurieren von "Programme hinzufügen/entfernen" mit Windows Installer</span><span class="sxs-lookup"><span data-stu-id="fa632-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="fa632-104">Sie können alle Informationen bereitstellen, die zum Konfigurieren von Software in der Systemsteuerung erforderlich sind, indem Sie die Werte bestimmter Installer-Eigenschaften im Windows Installer Paket der Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="fa632-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="fa632-105">Durch Festlegen dieser Eigenschaften werden die entsprechenden Werte automatisch in die Registrierung geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa632-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="fa632-106">Wenn das Installationsprogramm erkennt, dass das Produkt zum Abschluss der Löschung markiert ist, werden die Vorgänge automatisch dem Skript hinzugefügt, um den Ordner Software in den System Steuerungsinformationen für das Produkt zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fa632-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="fa632-107">Wenn eine Anwendung nicht registriert ist, wird Sie in der Systemsteuerung unter Software nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa632-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="fa632-108">Weitere Informationen finden Sie unter [Hinzufügen und Entfernen einer Anwendung und belassen der Registrierung in der Registrierung](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="fa632-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="fa632-109">Anwendungen, die im Einzelbenutzer [Installations Kontext](installation-context.md) installiert wurden, werden in der Option Software des aktuellen Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa632-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="fa632-110">Anwendungen, die im Installations Kontext pro Computer installiert wurden, werden in den Programmen Software aller Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa632-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="fa632-111">Anwendungen, die nicht pro Computer installiert wurden und nur als benutzerspezifische Anwendungen für andere Benutzer als den aktuellen Benutzer installiert wurden, werden nicht in den Programmen zum Hinzufügen/Entfernen des aktuellen Benutzers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa632-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="fa632-112">Beachten Sie, dass Installationspakete, die die [**limitui**](limitui.md) -Eigenschaft verwenden, auch das [**arpnomodify**](arpnomodify.md)-Objekt enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="fa632-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="fa632-113">Dies ist erforderlich, damit ein Benutzer das richtige Verhalten von der System Steuerungs Option "Software" beim Versuch, ein Produkt zu konfigurieren, erhält.</span><span class="sxs-lookup"><span data-stu-id="fa632-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="fa632-114">Das Installationsprogramm verwendet die folgenden [öffentlichen Eigenschaften](public-properties.md) zum Verwalten von Software in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="fa632-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa632-115">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="fa632-115">Property name</span></span></th>
<th><span data-ttu-id="fa632-116">Kurze Beschreibung der Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fa632-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa632-117"><a href="arpauthorizedcdfprefix.md"><strong>Arpauthorizedcdfprefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="fa632-118">Die URL des Aktualisierungs Kanals für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fa632-118">URL of the update channel for the application.</span></span> <span data-ttu-id="fa632-119">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-120"><a href="arpcomments.md"><strong>Arpcomments</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="fa632-121">Enthält Kommentare für die Option Software in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="fa632-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="fa632-122">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-123"><a href="arpcontact.md"><strong>Arpcontact</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="fa632-124">Stellt den Kontakt zum Hinzufügen/Entfernen von Programmen in der Systemsteuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="fa632-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="fa632-125">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-126"><a href="arpinstalllocation.md"><strong>Arpinstalllocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="fa632-127">Voll qualifizierter Pfad zum primären Ordner der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fa632-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="fa632-128">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-129"><a href="arphelplink.md"><strong>Arphelplink</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="fa632-130">Internet Adresse (URL), um technischen Support zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fa632-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="fa632-131">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-132"><a href="arphelptelephone.md"><strong>Arphelptelefon</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="fa632-133">Telefonnummern für technischen Support.</span><span class="sxs-lookup"><span data-stu-id="fa632-133">Technical support phone numbers.</span></span> <span data-ttu-id="fa632-134">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-135"><a href="arpnomodify.md"><strong>Arpnomodify</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="fa632-136">Verhindert, dass die Schaltfläche "ändern" für das Produkt in der Systemsteuerung unter "Software" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa632-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="fa632-137">
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus.</span><span class="sxs-lookup"><span data-stu-id="fa632-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="fa632-138">Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="fa632-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="fa632-140">Verhindert die Anzeige einer Entfernungs Schaltfläche für das Produkt in den Programmen "Software" in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="fa632-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="fa632-141">Das Produkt kann trotzdem entfernt werden, indem Sie die Schaltfläche ändern auswählen, wenn das Installationspaket mit einer Benutzeroberfläche erstellt wurde, die das Produkt entfernen als Option ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="fa632-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="fa632-142">
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus.</span><span class="sxs-lookup"><span data-stu-id="fa632-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="fa632-143">Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="fa632-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-144"><a href="arpnorepair.md"><strong>Arpnorepair</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="fa632-145">Deaktiviert die Schaltfläche reparieren in der Systemsteuerung unter Software.</span><span class="sxs-lookup"><span data-stu-id="fa632-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="fa632-146">
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus.</span><span class="sxs-lookup"><span data-stu-id="fa632-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="fa632-147">Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="fa632-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-148"><a href="arpproducticon.md"><strong>Arpproducticon</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="fa632-149">Identifiziert das Symbol, das unter "Software" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa632-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="fa632-150">Wenn diese Eigenschaft nicht definiert ist, gibt Add/Remove Software das Anzeige Symbol an.</span><span class="sxs-lookup"><span data-stu-id="fa632-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-151"><a href="arpreadme.md"><strong>Arpreadme</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="fa632-152">Stellt die Info für "Software" in der Systemsteuerung bereit.</span><span class="sxs-lookup"><span data-stu-id="fa632-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="fa632-153">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-154"><a href="arpsize.md"><strong>Arpsize</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="fa632-155">Geschätzte Größe der Anwendung in KB.</span><span class="sxs-lookup"><span data-stu-id="fa632-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="fa632-157">Verhindert, dass die Anwendung in der Liste Programme der Option Software in der Systemsteuerung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa632-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="fa632-158">
<b>Hinweis:</b> Dies wirkt sich nur auf die Anzeige im ARP aus.</span><span class="sxs-lookup"><span data-stu-id="fa632-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="fa632-159">Der Windows Installer ist weiterhin in der Lage, Anwendungen über eine Befehlszeile oder über die Programmierschnittstelle zu reparieren, zu installieren und zu deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="fa632-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa632-160"><a href="arpurlinfoabout.md"><strong>Arpurlinfoabout</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="fa632-161">URL für die Startseite der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fa632-161">URL for application's home page.</span></span> <span data-ttu-id="fa632-162">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa632-163"><a href="arpurlupdateinfo.md"><strong>Arpurlupdateinfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa632-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="fa632-164">URL für Anwendungs Update Informationen.</span><span class="sxs-lookup"><span data-stu-id="fa632-164">URL for application update information.</span></span> <span data-ttu-id="fa632-165">Der Wert, den das Installationsprogramm unter dem <a href="uninstall-registry-key.md">Deinstallations Registrierungsschlüssel</a>schreibt.</span><span class="sxs-lookup"><span data-stu-id="fa632-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="fa632-166">Weitere Informationen zum Tool Set Program und defaults finden Sie im Abschnitt [Arbeiten mit Festlegen des Programm Zugriffs und der Standardeinstellungen für Computer](/previous-versions//bb776877(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fa632-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa632-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa632-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa632-168">Registrierungsschlüssel deinstallieren</span><span class="sxs-lookup"><span data-stu-id="fa632-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
