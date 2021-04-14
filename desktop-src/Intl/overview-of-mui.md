---
description: Dieses Thema enthält eine konzeptionelle Übersicht über die Technologie für mehrsprachige Benutzeroberflächen (MUI), die Platt Form Unterstützung, die für die Aktivierung mehrsprachiger Benutzererfahrung bietet, und die Vorteile, die es für das Windows-Ökosystem bietet.
ms.assetid: ef828da8-61cd-43d9-a5fe-e09a1f8af5c7
title: Übersicht über MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674cb5e0fee4e7b8d3990a99f13f981c4a8c5803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565512"
---
# <a name="overview-of-mui"></a><span data-ttu-id="bd7d3-103">Übersicht über MUI</span><span class="sxs-lookup"><span data-stu-id="bd7d3-103">Overview of MUI</span></span>

<span data-ttu-id="bd7d3-104">Dieses Thema enthält eine konzeptionelle Übersicht über die Technologie für mehrsprachige Benutzeroberflächen (MUI), die Platt Form Unterstützung, die für die Aktivierung mehrsprachiger Benutzererfahrung bietet, und die Vorteile, die es für das Windows-Ökosystem bietet.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-104">This topic provides a conceptual overview of the Multilingual User Interface (MUI) technology, the platform support it provides for enabling multilingual user experiences, and the benefits it offers to the Windows ecosystem.</span></span>

<span data-ttu-id="bd7d3-105">Gehen Sie auf dieser Seite wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-105">On this page:</span></span>

-   [<span data-ttu-id="bd7d3-106">Die Notwendigkeit für mehrsprachige Computing</span><span class="sxs-lookup"><span data-stu-id="bd7d3-106">The need for multilingual computing</span></span>](#the-need-for-multilingual-computing)
-   [<span data-ttu-id="bd7d3-107">Die Rolle von MUI beim Aktivieren von mehrsprachigem Computing</span><span class="sxs-lookup"><span data-stu-id="bd7d3-107">The role of MUI in enabling multilingual computing</span></span>](#the-role-of-mui-in-enabling-multilingual-computing)
-   [<span data-ttu-id="bd7d3-108">Grundlegende Konzepte von MUI</span><span class="sxs-lookup"><span data-stu-id="bd7d3-108">Core concepts of MUI</span></span>](#core-concepts-of-mui)
-   [<span data-ttu-id="bd7d3-109">Verlauf von MUI in Windows</span><span class="sxs-lookup"><span data-stu-id="bd7d3-109">History of MUI in Windows</span></span>](#history-of-mui-in-windows)
-   [<span data-ttu-id="bd7d3-110">Vorteile der MUI-Technologie</span><span class="sxs-lookup"><span data-stu-id="bd7d3-110">Benefits of MUI technology</span></span>](#benefits-of-mui-technology)

## <a name="the-need-for-multilingual-computing"></a><span data-ttu-id="bd7d3-111">Die Notwendigkeit für mehrsprachige Computing</span><span class="sxs-lookup"><span data-stu-id="bd7d3-111">The need for multilingual computing</span></span>

<span data-ttu-id="bd7d3-112">Um von den in internationalen Märkten dargestellten Wachstumschancen zu profitieren, unterstützen die Plattformen und Anwendungen von Microsoft mehr Sprachen, Kulturen und Märkten als je zuvor.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-112">To benefit from the growth opportunities presented by international markets, Microsoft's platforms and applications support more languages, cultures and markets than ever before.</span></span>

<span data-ttu-id="bd7d3-113">Die Besonderheiten von Sprache, Kultur und Markt sind trotz zunehmender Globalisierungstrends weiterhin für internationale Benutzer äußerst wichtig.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-113">Language, culture, and market specifics are still extremely relevant to international users, despite increasing globalization trends.</span></span> <span data-ttu-id="bd7d3-114">Das folgende Kreis Diagramm zeigt, dass nicht englische Referenten nach wie vor 91,5 Prozent der Bevölkerung der Welt ausmachen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-114">The following pie chart shows that non-English speakers still make up 91.5 percent of the world's population.</span></span>

![Kreis Diagramm mit drei Segmenten; die Bezeichnung "nicht englischsprachige Sprecher 91,5%" ist weitaus größer als die beiden anderen, kombiniert](images/overview-of-mui-fig1.gif)

<span data-ttu-id="bd7d3-116">Weltweit sind heute 193 Länder und mehr als 6.900 bekannte lebende Sprachen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-116">Worldwide, there are 193 countries and over 6,900 known living languages in use today.</span></span> <span data-ttu-id="bd7d3-117">Englisch, trotz seiner Rolle als Geschäftssprache der Welt, wird nur von 8,5% der Bevölkerung der Welt als erste oder zweite Sprache gesprochen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-117">English, despite its role as the world's business language, is only spoken by 8.5% of the world's population as a first or second language.</span></span> <span data-ttu-id="bd7d3-118">Um systemeigene Informationen für 94% der Einwohner Welt bereitzustellen, müssen diese Informationen in 347 (ca. 5%) verfügbar sein. der Sprachen der Welt, die über mindestens eine Million Referenten verfügen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-118">To provide native information to 94% of the world's population, this information would need to be available in the 347 (about 5%) of the world's languages that have at least a million speakers.</span></span> <span data-ttu-id="bd7d3-119">Dies trifft vor allem dann zu, wenn Globalisierungstrends die Erwartungen dieser Benutzer hinsichtlich der Technologie und ihrer Verfügbarkeit in ihren Märkten gesteigert haben.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-119">This is especially true as globalization trends have increased the expectations of these users regarding technology and its availability in their markets.</span></span>

<span data-ttu-id="bd7d3-120">Die Notwendigkeit, Software in mehr Sprachen zu lokalisieren, hat sich im Laufe der Jahre gesteigert, und Microsoft stellt nun Windows Vista und andere Produkte in mehr Sprachen bereit als je zuvor.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-120">The need to localize software in more languages has increased over the years and Microsoft is now providing Windows Vista and other products in more languages than ever.</span></span> <span data-ttu-id="bd7d3-121">Diese Entwicklung ist insbesondere bei Microsoft Windows eindeutig, da es von der Unterstützung von 30 Sprachen mit Windows 98 bis fast 100 mit Windows Vista ging, wie im folgenden Balkendiagramm veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-121">This evolution is especially clear with Microsoft Windows, as it has gone from supporting 30 languages with Windows 98 to almost 100 with Windows Vista, as illustrated in the following bar chart.</span></span>

![Balkendiagramm, das anzeigt, dass die Anzahl der Sprachen in Windows Vista viel größer ist als in Windows 98 oder Windows XP](images/overview-of-mui-fig2.gif)

<span data-ttu-id="bd7d3-123">*Abbildung 2 – Anzahl der von Microsoft Windows-Versionen unterstützten Sprachen*</span><span class="sxs-lookup"><span data-stu-id="bd7d3-123">*Figure 2—Number of languages supported by Microsoft Windows releases*</span></span>

## <a name="the-role-of-mui-in-enabling-multilingual-computing"></a><span data-ttu-id="bd7d3-124">Die Rolle von MUI beim Aktivieren von mehrsprachigem Computing</span><span class="sxs-lookup"><span data-stu-id="bd7d3-124">The role of MUI in enabling multilingual computing</span></span>

<span data-ttu-id="bd7d3-125">Wie bereits im vorherigen Abschnitt erläutert wurde, sind [Globalisierung](glossary-for-understanding-mui.md) und [Lokalisierung](glossary-for-understanding-mui.md) von Anwendungen in einer global integrierten Welt zu einer Notwendigkeit geworden.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-125">As discussed in the previous section, [globalization](glossary-for-understanding-mui.md) and [localization](glossary-for-understanding-mui.md) of applications have become a necessity in a more globally integrated world.</span></span> <span data-ttu-id="bd7d3-126">Da immer mehr Unternehmen sowohl intern als auch über Ihre Unternehmensnetzwerke Global sind, wird der Bedarf an mehrsprachigen Anwendungen erheblich erhöht.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-126">In particular, as more and more enterprises are going global, either internally or through their business networks, the need for multi-lingual applications is increasing dramatically.</span></span> <span data-ttu-id="bd7d3-127">Dies sind die Hürden, die diese Unternehmen bei der globalen Bereitstellung dieser Anwendungen unterliegen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-127">So are the hurdles that these companies currently face in deploying these applications globally.</span></span>

<span data-ttu-id="bd7d3-128">Um Unterstützung für mehr Sprachen für Windows-Betriebssysteme sowie für die Windows-Plattform entwickelte Softwareanwendungen bereitzustellen, sind neue Strategien erforderlich, mit denen alle wichtigen Szenarien mit minimalem Engineering-Aufwand implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-128">Providing support for more languages for Windows operating systems, as well as software applications built for the Windows platform, requires new strategies which enable all major scenarios to be implemented with minimal engineering overhead.</span></span>

<span data-ttu-id="bd7d3-129">Die MUI-Technologie richtet sich an Entwickler und ISVs, die auf die Erstellung und Unterstützung mehrsprachiger Anwendungen für die Windows-Plattform abzielen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-129">MUI technology is targeted at developers and ISVs aiming to build and support multilingual applications for the Windows platform.</span></span> <span data-ttu-id="bd7d3-130">MUI ist auch eine wichtige Bedeutung für OEMs und Unternehmen, die Sie zum Bereitstellen des Windows-Betriebssystems und zum Hinzufügen von Anwendungen zu Computern in verschiedenen Sprachen durch Bereitstellung mit nur einem Image nutzen können.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-130">MUI is also of key significance to OEMs and enterprises, who can leverage it to deploy the Windows operating system and add applications to computers across different languages through single image deployment.</span></span>

## <a name="core-concepts-of-mui"></a><span data-ttu-id="bd7d3-131">Grundlegende Konzepte von MUI</span><span class="sxs-lookup"><span data-stu-id="bd7d3-131">Core concepts of MUI</span></span>

<span data-ttu-id="bd7d3-132">Die grundlegende Idee hinter MUI besteht darin, [den Speicher Lokalisier barer Ressourcen aus dem](mui-fundamental-concepts-explained.md)Quellcode der Anwendung zu trennen, damit jede mehrsprachige Anwendung als eine Kombination aus einer sprach neutralen kernbinär Datei und einer Reihe von sprachspezifischen lokalisierten Ressourcen Dateien konzipiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-132">The fundamental idea behind MUI is to [separate the storage of localizable resources from application source code](mui-fundamental-concepts-explained.md), so as to be able to architect any multilingual application as a combination of a language-neutral core binary and a set of language-specific localized resource files.</span></span>

<span data-ttu-id="bd7d3-133">Sobald der Quellcode der Anwendung getrennt von den lokalisierten Ressourcen gespeichert wird, ist es einfach, [die geeigneten lokalisierten Ressourcen](mui-fundamental-concepts-explained.md) für einen bestimmten Anwendungskontext dynamisch zu laden, basierend auf einer Logik, die System-, Benutzer-und Anwendungsebene für die Benutzeroberflächen Sprache berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-133">Once application source code is stored separately from the localized resources, it becomes easy to [dynamically load the appropriate localized resources](mui-fundamental-concepts-explained.md) for a given application context based on a logic that takes into account system, user and application-level settings for the user interface language.</span></span>

<span data-ttu-id="bd7d3-134">Diese grundlegenden Attribute von MUI helfen, Geschäftsszenarien wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-134">These fundamental attributes of MUI help facilitate business scenarios such as:</span></span>

-   <span data-ttu-id="bd7d3-135">Ein verbessertes Lokalisierungs Modell für die Benutzeroberfläche und den Hilfe Inhalt über die physische Trennung von Quellcode der Anwendung und Lokalisier barer Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-135">An improved localization model for user interface and help content, via the physical separation of application source code and localizable resources.</span></span>
-   <span data-ttu-id="bd7d3-136">Behandeln Lokalisier barer Ressourcen als dynamischer Inhalt und Laden dieser Ressourcen entsprechend den Einstellungen der Benutzeroberflächen Sprache und den Fall Back Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-136">Treating the localizable resources as dynamic content and loading them according to the UI language settings and fallback preferences.</span></span> <span data-ttu-id="bd7d3-137">Dies ermöglicht Szenarien wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-137">This enables scenarios such as:</span></span>
    -   <span data-ttu-id="bd7d3-138">Wechseln zur Laufzeit von einer Benutzeroberflächen Sprache zu einer anderen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-138">Switching from one UI language to another one at run-time.</span></span>
    -   <span data-ttu-id="bd7d3-139">Erstellen regionaler oder weltweit einstellungsimages, die eine Reihe von Sprachen für OEMs und Unternehmen abdecken.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-139">Creating regional or worldwide single deployment images that cover a set of languages for OEMs and enterprises.</span></span>

## <a name="history-of-mui-in-windows"></a><span data-ttu-id="bd7d3-140">Verlauf von MUI in Windows</span><span class="sxs-lookup"><span data-stu-id="bd7d3-140">History of MUI in Windows</span></span>

<span data-ttu-id="bd7d3-141">Die Unterstützung für mehrsprachige Benutzer auf der Windows-Betriebssystemebene und für die mehrsprachige Anwendungsentwicklung auf der Windows-Plattform hat sich im Laufe der Zeit und über die verschiedenen Versionen von Windows entwickelt.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-141">The level of support available for a multilingual user experience at the Windows operating system level and for multilingual application development on the Windows platform has evolved over time and across the different versions of Windows.</span></span>

<span data-ttu-id="bd7d3-142">Die unterstützte Funktionalität [vor Windows Vista](evolution-of-mui-support-across-windows-versions.md) war relativ einfach, mit einsprachigen Windows-Images und einer Option zum Hinzufügen von mehrsprachigen Benutzerschnittstellen Paketen in bestimmten Szenarien.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-142">The supported functionality [before Windows Vista](evolution-of-mui-support-across-windows-versions.md) was fairly basic, with single-language Windows images and an option to add-on Multilingual User Interface Packs in specific scenarios.</span></span> <span data-ttu-id="bd7d3-143">Es war keine Entwickler Unterstützung für mehrsprachige Anwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-143">No developer support for multilingual applications was available.</span></span>

<span data-ttu-id="bd7d3-144">[Mit Windows Vista](evolution-of-mui-support-across-windows-versions.md)machte Microsoft bedeutende Investitionen in MUI, und Windows Vista wurde von Grund auf auf einer MUI-Plattform erstellt.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-144">[With Windows Vista](evolution-of-mui-support-across-windows-versions.md), Microsoft made a significant investment in MUI, and Windows Vista is built from the ground up on a MUI platform.</span></span> <span data-ttu-id="bd7d3-145">Obwohl dies ein wichtiger Fortschritt bei der Windows-Lokalisierungsstrategie darstellt, ist es ein wichtiger Faktor für Microsoft, Windows in mehr Sprachen als je zuvor bereitzustellen, und es ist vor allem eine gute Voraussetzung für Windows-Benutzer,-Entwickler und-Kunden.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-145">While this represents a major advance in Windows localization strategy, as it is a key enabler for Microsoft to provide Windows in more languages than ever before, it is first and foremost a great advance for Windows users, developers, and customers.</span></span> <span data-ttu-id="bd7d3-146">Dies bietet verschiedene wichtige Vorteile, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-146">It provides several major benefits such as:</span></span>

-   <span data-ttu-id="bd7d3-147">Ein sprach neutrales Betriebssystem mit integrierter Unterstützung für MUI.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-147">A language-neutral operating system with built-in support for MUI.</span></span>
-   <span data-ttu-id="bd7d3-148">Konfigurierbare Paket Erstellung, Bereitstellung und Installation, um mehrsprachige Szenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-148">Configurable packaging, deployment, and installation to support multilingual scenarios.</span></span>
-   <span data-ttu-id="bd7d3-149">Bereitstellung mit einem Bild mit mehreren Sprachen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-149">Single-image deployment with multiple languages.</span></span>
-   <span data-ttu-id="bd7d3-150">Ein verbessertes Wartungs Modell, bei dem der ausführbare Code unabhängig von den Ressourcen aktualisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-150">An improved servicing model where the executable code can be updated independently of the resources.</span></span>
-   <span data-ttu-id="bd7d3-151">Entwickler Unterstützung zum entwickeln mehrsprachiger Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-151">Developer support for building multilingual applications.</span></span>

<span data-ttu-id="bd7d3-152">In der folgenden Tabelle finden Sie eine ausführliche Übersicht über die Unterstützung der Windows-Plattform für MUI:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-152">The following table provides a detailed overview of the Windows platform support for MUI:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd7d3-153">Category</span><span class="sxs-lookup"><span data-stu-id="bd7d3-153">Category</span></span></th>
<th><span data-ttu-id="bd7d3-154">Support</span><span class="sxs-lookup"><span data-stu-id="bd7d3-154">Support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd7d3-155">Unterstützte Windows-Versionen (nur Betriebssystemunterstützung)</span><span class="sxs-lookup"><span data-stu-id="bd7d3-155">Supported Windows versions (OS support only)</span></span></td>
<td><ul>
<li><span data-ttu-id="bd7d3-156">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bd7d3-156">Windows 2000 Professional</span></span></li>
<li><span data-ttu-id="bd7d3-157">Windows 2000-Server Familie</span><span class="sxs-lookup"><span data-stu-id="bd7d3-157">Windows 2000 Server family</span></span></li>
<li><span data-ttu-id="bd7d3-158">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="bd7d3-158">Windows XP Professional</span></span></li>
<li><span data-ttu-id="bd7d3-159">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="bd7d3-159">Windows XP Tablet PC Edition</span></span></li>
<li><span data-ttu-id="bd7d3-160">Windows Server 2003-Produktfamilie</span><span class="sxs-lookup"><span data-stu-id="bd7d3-160">Windows Server 2003 family</span></span></li>
<li><span data-ttu-id="bd7d3-161">Windows XP Embedded</span><span class="sxs-lookup"><span data-stu-id="bd7d3-161">Windows XP Embedded</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd7d3-162">Unterstützte Windows-Versionen (Unterstützung für Betriebssystem & Anwendungen)</span><span class="sxs-lookup"><span data-stu-id="bd7d3-162">Supported Windows versions (OS & application support)</span></span></td>
<td><ul>
<li><span data-ttu-id="bd7d3-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd7d3-163">Windows Vista</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd7d3-164">Nicht Unterstützte Windows-Versionen</span><span class="sxs-lookup"><span data-stu-id="bd7d3-164">Unsupported Windows versions</span></span></td>
<td><ul>
<li><span data-ttu-id="bd7d3-165">Windows 9X</span><span class="sxs-lookup"><span data-stu-id="bd7d3-165">Windows 9x</span></span></li>
<li><span data-ttu-id="bd7d3-166">Windows Me</span><span class="sxs-lookup"><span data-stu-id="bd7d3-166">Windows Me</span></span></li>
<li><span data-ttu-id="bd7d3-167">Windows XP Home Edition</span><span class="sxs-lookup"><span data-stu-id="bd7d3-167">Windows XP Home Edition</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="benefits-of-mui-technology"></a><span data-ttu-id="bd7d3-168">Vorteile der MUI-Technologie</span><span class="sxs-lookup"><span data-stu-id="bd7d3-168">Benefits of MUI technology</span></span>

<span data-ttu-id="bd7d3-169">MUI wirkt sich positiv auf mehrere Aspekte des Windows-Ökosystems aus:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-169">MUI positively impacts multiple aspects of the Windows ecosystem:</span></span>

-   <span data-ttu-id="bd7d3-170">[Vorteile für Entwickler](benefits-of-mui-explained.md): zahlreiche Vorteile von Anwendungsentwicklern durch die Verfügbarkeit der MUI-API-Unterstützung, um mehrsprachige Anwendungen zu erstellen, die auf denselben Prinzipien basieren wie die mehrsprachige Unterstützung im Windows-Kernbetriebssystem.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-170">[Benefits for Developers](benefits-of-mui-explained.md): Numerous benefits are offered to application developers by the availability of MUI API support to build multilingual applications modeled on the same principles as the multilingual support in the core Windows operating system itself.</span></span> <span data-ttu-id="bd7d3-171">Zu diesen Vorteilen zählen:</span><span class="sxs-lookup"><span data-stu-id="bd7d3-171">These benefits include:</span></span>
    -   <span data-ttu-id="bd7d3-172">Die Möglichkeit, eine Anzeige Sprache bereitzustellen, die mit den Funktionen des Betriebssystems konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-172">The ability to provide a display language experience that is consistent with what the operating system itself offers.</span></span>
    -   <span data-ttu-id="bd7d3-173">Die Möglichkeit, die Sprachunterstützung für eine Anwendung auf einfache Weise zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-173">The ability to easily extend the language support for an application.</span></span>
    -   <span data-ttu-id="bd7d3-174">Die Möglichkeit, die Anwendung leicht zu verwalten und zu warten.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-174">The ability to easily maintain and service the application.</span></span>
    -   <span data-ttu-id="bd7d3-175">Die Möglichkeit, die Bereitstellung von Anwendungen mit nur einem Image durch OEMs zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-175">The ability to enable single-image deployment of applications by OEMs.</span></span>
-   <span data-ttu-id="bd7d3-176">[Vorteile für Unternehmen](benefits-of-mui-explained.md): der größte Vorteil, den MUI für Unternehmen bietet, ist die Möglichkeit, das gleiche mehrsprachige Image weltweit mit einer einzelnen Installation einzuführen, zu unterstützen und zu pflegen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-176">[Benefits for Enterprises](benefits-of-mui-explained.md): The major benefit that MUI offers for enterprises is the ability to roll out, support, and maintain the same multilingual image worldwide with a single installation.</span></span> <span data-ttu-id="bd7d3-177">Ein weiterer bedeutender Gewinn ist die Möglichkeit, mehrsprachige Desktops zu unterstützen, die eine nahtlose Interaktion mit Benutzern mit unterschiedlichen Spracheinstellungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-177">Another significant win is the ability to support multilingual desktops that offer seamless interaction to users with different language preferences.</span></span>
-   <span data-ttu-id="bd7d3-178">[Vorteile für OEMs](benefits-of-mui-explained.md): der größte Vorteil für OEMs ist die Installation mit einem einzelnen Image, die MUI ermöglicht, mit Unterstützung für mehrere Sprachen, die eine effektivere Verwaltung der Inventur ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-178">[Benefits for OEMs](benefits-of-mui-explained.md): The major benefit for OEMs is the single image installation that MUI enables, with support for multiple languages, which enables a more effective management of inventory.</span></span> <span data-ttu-id="bd7d3-179">OEMs profitieren auch von der MUI-Unterstützung für die Anwendungsentwicklung, da Sie Ihnen die Bereitstellung von Mehrwert Anwendungen auf Ihren Images ermöglicht, während Sie von der Installation mit einem einzelnen Image profitieren, solange diese Anwendungen MUI-fähig sind.</span><span class="sxs-lookup"><span data-stu-id="bd7d3-179">OEMs also benefit from the MUI support for application development, as it enables them to provide value-add applications on their images while benefiting from the single image installation, as long as these applications are MUI-enabled.</span></span>

 

 




