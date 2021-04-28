---
description: Entfernen von Windows-E-Mail
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Entfernen von Windows-E-Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50ad1008d9e252e1705a159f19d362677934023
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116278"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="86c9a-103">Entfernen von Windows-E-Mail</span><span class="sxs-lookup"><span data-stu-id="86c9a-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="86c9a-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="86c9a-104">Affected Platforms</span></span>

<span data-ttu-id="86c9a-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="86c9a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="86c9a-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86c9a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="86c9a-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="86c9a-107">Feature Impact</span></span>

<span data-ttu-id="86c9a-108">**Schweregrad:** Hoch</span><span class="sxs-lookup"><span data-stu-id="86c9a-108">**Severity** - High</span></span>  
<span data-ttu-id="86c9a-109">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="86c9a-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="86c9a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86c9a-110">Description</span></span>

<span data-ttu-id="86c9a-111">Microsoft stellt das Windows Mail-Hilfsprogramm als veraltet ein und deaktiviert die API CoStartOutlookExpress.</span><span class="sxs-lookup"><span data-stu-id="86c9a-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="86c9a-112">Die anderen E-Mail-APIs wurden als veraltet markiert und werden in einer späteren Windows-Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="86c9a-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="86c9a-113">Die öffentlich dokumentierten APIs, die nicht als veraltet oder veraltet markiert sind, funktionieren in Windows 7 jedoch weiterhin.</span><span class="sxs-lookup"><span data-stu-id="86c9a-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="86c9a-114">Binärdateien verbleiben auf den Systemen der Benutzer und sind weiterhin über die APIs zugänglich, insbesondere in den oben genannten Fällen.</span><span class="sxs-lookup"><span data-stu-id="86c9a-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="86c9a-115">Darüber hinaus verbleiben die E-Mail- (EML) und News-Dateien (.nws) der Benutzer auf dem System.</span><span class="sxs-lookup"><span data-stu-id="86c9a-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="86c9a-116">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="86c9a-116">Manifestation of Impact</span></span>

<span data-ttu-id="86c9a-117">Das Entfernen von Windows Mail führt zu Folgendem:</span><span class="sxs-lookup"><span data-stu-id="86c9a-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="86c9a-118">Alle Einstiegspunkte für Windows-E-Mail und -Kontakte (z. B. Startmenü, vom Benutzer erstellte Verknüpfungen, Start -> Ausführen und so weiter) werden entfernt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="86c9a-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="86c9a-119">Einige davon werden vollständig entfernt, andere werden beim Versuch, gestartet zu werden, fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="86c9a-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="86c9a-120">Alle DLLs sind im Feld</span><span class="sxs-lookup"><span data-stu-id="86c9a-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="86c9a-121">Öffentlich dokumentierte APIs funktionieren weiterhin wie in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86c9a-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="86c9a-122">Alle APIs, die versuchen, die Hauptbenutzeroberfläche des Browsers zu starten, wurden geändert, um einen automatischen Fehler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="86c9a-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="86c9a-123">Die Funktion gibt den Erfolg zurück, zeigt dem Benutzer jedoch nicht die Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="86c9a-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="86c9a-124">APIs, die andere Dialogfelder aufrufen (z. B. der Spooler oder das Dialogfeld Konten), zeigen diese Benutzeroberfläche weiterhin an.</span><span class="sxs-lookup"><span data-stu-id="86c9a-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="86c9a-125">Protokollhandler (mailto, ldap, news, sara, nntp) werden windows-E-Mail oder -Kontakten nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="86c9a-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="86c9a-126">Wenn Sie versuchen, diese zu starten, wird kunden ein Fehlerdialogfeld angezeigt, das sie auf den Speicherort der Zuordnungen zu einem anderen Programm verweisen kann.</span><span class="sxs-lookup"><span data-stu-id="86c9a-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="86c9a-127">Dateizuordnungen (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) sind beschädigt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="86c9a-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="86c9a-128">Wenn Sie versuchen, eine Datei mit diesen Erweiterungen zu öffnen, erhalten Kunden ein Dialogfeld, das ihnen andere installierte Apps anbietet, die sie verwenden und auf eine Webseite verweisen können, die Lösungen anbietet.</span><span class="sxs-lookup"><span data-stu-id="86c9a-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="86c9a-129">Alle Benutzerdateien (z. B. Kontaktdateien oder Nachrichten) verbleiben im Upgradeszenario auf dem System.</span><span class="sxs-lookup"><span data-stu-id="86c9a-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="86c9a-130">Der Ordner "Kontakte" ist standardmäßig ausgeblendet, sodass Kunden ihn nicht sehen.</span><span class="sxs-lookup"><span data-stu-id="86c9a-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="86c9a-131">APIs sind in MSDN als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="86c9a-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="86c9a-132">Die Dateivorschaufunktion wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86c9a-132">The file preview function is removed</span></span>
-   <span data-ttu-id="86c9a-133">Shellhooks im Kontextmenü werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="86c9a-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="86c9a-134">Die Dateisuchfunktion wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="86c9a-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="86c9a-135">Minderung</span><span class="sxs-lookup"><span data-stu-id="86c9a-135">Mitigation</span></span>

<span data-ttu-id="86c9a-136">Benutzer sollten Windows Live Mail oder ein anderes E-Mail-Produkt installieren, das EML- und NWS-Dateien lesen kann.</span><span class="sxs-lookup"><span data-stu-id="86c9a-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="86c9a-137">Lösung</span><span class="sxs-lookup"><span data-stu-id="86c9a-137">Solution</span></span>

<span data-ttu-id="86c9a-138">Ermitteln Sie, ob ein Standard-E-Mail-Handler installiert ist.</span><span class="sxs-lookup"><span data-stu-id="86c9a-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="86c9a-139">Wenn dies nicht der Fall ist, empfehlen Sie dem Benutzer, Windows Live Mail oder ein anderes Produkt zu installieren, das EML- und NWS-Dateien lesen kann.</span><span class="sxs-lookup"><span data-stu-id="86c9a-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="86c9a-140">Entwerfen Sie keinen Code, der die Windows Mail-UI-API aufruft, da sie nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="86c9a-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="86c9a-141">Sie müssen andere Möglichkeiten für den Zugriff auf die EML- und NWS-Dateien finden.</span><span class="sxs-lookup"><span data-stu-id="86c9a-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="86c9a-142">Stellen Sie außerdem, sobald dies möglich ist, ihre Abhängigkeit von allen anderen Windows Mail-APIs ein.</span><span class="sxs-lookup"><span data-stu-id="86c9a-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="86c9a-143">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests</span><span class="sxs-lookup"><span data-stu-id="86c9a-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="86c9a-144">Führen Sie Ihre Anwendung in einer Windows 7-Umgebung aus, um sicherzustellen, dass die Anwendung nicht versucht, die UI-API auf aufruft.</span><span class="sxs-lookup"><span data-stu-id="86c9a-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="86c9a-145">Alternativ können Sie das Application Compatibility Toolkit (ACT) mithilfe der Windows-Kompatibilitätsauswertung (Windows Compatibility Evaluator, WCE) ausführen, um mögliche Probleme zu ermitteln, die durch die Veralterung dieser Funktionalität bedingt sind.</span><span class="sxs-lookup"><span data-stu-id="86c9a-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="86c9a-146">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86c9a-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="86c9a-147">Download des Anwendungskompatibilitätstoolkits</span><span class="sxs-lookup"><span data-stu-id="86c9a-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
