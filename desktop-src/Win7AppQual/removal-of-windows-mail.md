---
description: .
ms.assetid: 356f0d79-12dd-49f0-b756-a46f20177efa
title: Entfernen von Windows Mail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836b2f447735c8e3595955ca7e99f1ae818c3d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217981"
---
# <a name="removal-of-windows-mail"></a><span data-ttu-id="927d1-103">Entfernen von Windows Mail</span><span class="sxs-lookup"><span data-stu-id="927d1-103">Removal of Windows Mail</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="927d1-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="927d1-104">Affected Platforms</span></span>

<span data-ttu-id="927d1-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="927d1-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="927d1-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="927d1-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="927d1-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="927d1-107">Feature Impact</span></span>

<span data-ttu-id="927d1-108">**Schweregrad** -hoch</span><span class="sxs-lookup"><span data-stu-id="927d1-108">**Severity** - High</span></span>  
<span data-ttu-id="927d1-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="927d1-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="927d1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="927d1-110">Description</span></span>

<span data-ttu-id="927d1-111">Microsoft hat das Windows Mail-Hilfsprogramm als veraltet markiert und die API costartoutlookexpress deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d1-111">Microsoft is deprecating the Windows Mail utility and disabling the API CoStartOutlookExpress.</span></span> <span data-ttu-id="927d1-112">Die anderen e-Mail-APIs wurden als veraltet markiert und können in einer späteren Windows-Version entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="927d1-112">The other mail APIs have been marked as deprecated and are slated for removal in a later Windows version.</span></span> <span data-ttu-id="927d1-113">Die öffentlich dokumentierten APIs, die nicht als veraltet oder veraltet gekennzeichnet sind, werden jedoch weiterhin in Windows 7 funktionieren.</span><span class="sxs-lookup"><span data-stu-id="927d1-113">However, the publicly documented APIs that are not marked as deprecated or obsolete will continue to function in Windows 7.</span></span> <span data-ttu-id="927d1-114">Binärdateien bleiben in den Benutzer Systemen erhalten und können weiterhin über die APIs aufgerufen werden, insbesondere in den oben erwähnten Fällen.</span><span class="sxs-lookup"><span data-stu-id="927d1-114">Binaries will remain on the users' systems and will continue to be accessible via the APIs, specifically in the cases mentioned above.</span></span> <span data-ttu-id="927d1-115">Außerdem verbleiben die e-Mail-Dateien (. eml) und Nachrichten Dateien (. NWS) des Benutzers auf dem System.</span><span class="sxs-lookup"><span data-stu-id="927d1-115">In addition, the users' email (.eml) and news (.nws) files will remain on the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="927d1-116">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="927d1-116">Manifestation of Impact</span></span>

<span data-ttu-id="927d1-117">Das Entfernen von Windows Mail führt zu folgendem:</span><span class="sxs-lookup"><span data-stu-id="927d1-117">Removal of Windows Mail results in the following:</span></span>

-   <span data-ttu-id="927d1-118">Alle Einstiegspunkte für Windows-e-Mail und-Kontakte (z. b. Startmenü, von Benutzern erstellte Verknüpfungen, Start > ausführen usw.) werden entfernt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d1-118">All entry points to Windows Mail and Contacts (for example, Start Menu, user-created Shortcuts, Start -> Run, and so on) are removed or disabled.</span></span> <span data-ttu-id="927d1-119">Einige davon werden vollständig entfernt, andere schlagen bei dem Versuch, zu starten, fehl.</span><span class="sxs-lookup"><span data-stu-id="927d1-119">Some of these are completely removed, others will fail when trying to launch.</span></span>
-   <span data-ttu-id="927d1-120">Alle DLLs werden in der Box ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="927d1-120">All DLLs ship in the box</span></span>
-   <span data-ttu-id="927d1-121">Öffentlich dokumentierte APIs funktionieren weiterhin wie in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="927d1-121">Publicly documented APIs continue to work as they did in Windows Vista</span></span>
-   <span data-ttu-id="927d1-122">Alle APIs, die versuchen, die Hauptbenutzer Oberfläche des Browsers zu starten, wurden geändert, um einen automatischen Fehler zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="927d1-122">Any APIs that attempt to launch the main browser UI have been modified to create a silent failure.</span></span> <span data-ttu-id="927d1-123">Die Funktion gibt Erfolg zurück, zeigt jedoch nicht die Benutzeroberfläche für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="927d1-123">The function will return success, but will not show the UI to the user.</span></span> <span data-ttu-id="927d1-124">APIs, die andere Dialogfelder (z. b. Spooler oder das Dialogfeld "Konten") aufzurufen, zeigen die Benutzeroberfläche weiterhin an.</span><span class="sxs-lookup"><span data-stu-id="927d1-124">APIs that call other dialog boxes (for example, the Spooler or the Accounts dialog) continue to show that UI</span></span>
-   <span data-ttu-id="927d1-125">Protokollhandler (mailto, LDAP, News, sNews, NNTP) werden nicht mit Windows Mail oder Kontakten verknüpft.</span><span class="sxs-lookup"><span data-stu-id="927d1-125">Protocol (mailto, ldap, news, snews, nntp) handlers will not be associated with Windows Mail or Contacts.</span></span> <span data-ttu-id="927d1-126">Wenn Sie versuchen, diese zu starten, wird ein Fehler Dialogfeld angezeigt, das Sie auf den Speicherort zeigt, an dem diese Zuordnungen auf ein anderes Programm festlegen können</span><span class="sxs-lookup"><span data-stu-id="927d1-126">When attempting to launch these, customers will see an error dialog pointing them to the location where they can set these associations to another program</span></span>
-   <span data-ttu-id="927d1-127">Dateizuordnungen (. eml,. nws,. Contact,. Group,. wab,. P7C,. VFC) sind beschädigt oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="927d1-127">File associations (.eml, .nws, .contact, .group, .wab, .p7c, .vfc) are broken or disabled.</span></span> <span data-ttu-id="927d1-128">Wenn Sie versuchen, eine Datei mit diesen Erweiterungen zu öffnen, erhalten Kunden ein Dialogfeld mit anderen installierten apps, die Sie verwenden und auf eine Webseite verweisen können, die Lösungen anbietet.</span><span class="sxs-lookup"><span data-stu-id="927d1-128">When attempting to open a file with these extensions, customers will get a dialog box offering them other apps that are installed that they can use and point them to a webpage that offers solutions</span></span>
-   <span data-ttu-id="927d1-129">Alle Benutzer Dateien (z. b. Kontakt Dateien oder Meldungen) verbleiben im Upgradeszenario im System.</span><span class="sxs-lookup"><span data-stu-id="927d1-129">Any user files (for example, contact files or messages) remain on the system in the upgrade scenario</span></span>
-   <span data-ttu-id="927d1-130">Der Ordner "Contacts" ist standardmäßig ausgeblendet, sodass er von Kunden nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="927d1-130">The Contacts folder is hidden by default so customers will not see it</span></span>
-   <span data-ttu-id="927d1-131">APIs werden in MSDN als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="927d1-131">APIs are marked as deprecated in MSDN</span></span>
-   <span data-ttu-id="927d1-132">Die Datei Vorschau Funktion wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="927d1-132">The file preview function is removed</span></span>
-   <span data-ttu-id="927d1-133">Shellhooks im Kontextmenü werden entfernt</span><span class="sxs-lookup"><span data-stu-id="927d1-133">Shell hooks in the right-click menu are removed</span></span>
-   <span data-ttu-id="927d1-134">Die Datei Suchfunktion wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="927d1-134">The file search function is removed</span></span>

## <a name="mitigation"></a><span data-ttu-id="927d1-135">Minderung</span><span class="sxs-lookup"><span data-stu-id="927d1-135">Mitigation</span></span>

<span data-ttu-id="927d1-136">Benutzer sollten Windows Live Mail oder ein anderes Mail Produkt installieren, das. eml-und nws-Dateien lesen kann.</span><span class="sxs-lookup"><span data-stu-id="927d1-136">Users should install Windows Live Mail or any other mail product that is able to read .eml and .nws files.</span></span>

## <a name="solution"></a><span data-ttu-id="927d1-137">Lösung</span><span class="sxs-lookup"><span data-stu-id="927d1-137">Solution</span></span>

<span data-ttu-id="927d1-138">Erkennen, ob ein Standard-e-Mail-Handler installiert ist.</span><span class="sxs-lookup"><span data-stu-id="927d1-138">Detect if there is a default mail handler installed.</span></span> <span data-ttu-id="927d1-139">Wenn dies nicht der Wert ist, sollten Sie den Benutzer dazu informieren, Windows Live Mail oder ein anderes Produkt zu installieren, das. eml-und nws-Dateien lesen kann.</span><span class="sxs-lookup"><span data-stu-id="927d1-139">If not, advise user to install Windows Live Mail or any other product that is able to read .eml and .nws files.</span></span>

<span data-ttu-id="927d1-140">Entwerfen Sie keinen Code, der die Benutzeroberflächen-API von Windows Mail aufruft, da dies nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="927d1-140">Do not design code that calls the Windows Mail UI API, since it will not work.</span></span> <span data-ttu-id="927d1-141">Sie müssen weitere Möglichkeiten finden, um auf die EML-und nws-Dateien zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="927d1-141">You must find other ways to access the .eml and .nws files.</span></span> <span data-ttu-id="927d1-142">Außerdem müssen Sie, sobald dies möglich ist, ihre Abhängigkeit von allen anderen Windows Mail-APIs beenden.</span><span class="sxs-lookup"><span data-stu-id="927d1-142">In addition, as soon as is feasible, discontinue your reliance on all other Windows Mail APIs.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="927d1-143">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="927d1-143">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="927d1-144">Testen Sie Ihre Anwendung in einer Windows 7-Umgebung, um sicherzustellen, dass die Anwendung nicht versucht, die UI-API aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="927d1-144">Exercise your application in a Windows 7 environment to ensure that the application does not try to call the UI API.</span></span>
-   <span data-ttu-id="927d1-145">Alternativ können Sie das Anwendungskompatibilitäts-Toolkit (Act) mithilfe von Windows Compatibility Evaluator (WCE) ausführen, um mögliche Probleme aufgrund der Veraltung dieser Funktionalität zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="927d1-145">Alternatively, you can run the Application Compatibility Toolkit (ACT) using the Windows Compatibility Evaluator (WCE) to locate any potential issues due to the deprecation of this functionality.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="927d1-146">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="927d1-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="927d1-147">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="927d1-147">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)  
</dl>

 

 
