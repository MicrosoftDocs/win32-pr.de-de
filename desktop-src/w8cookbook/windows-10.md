---
title: Windows 10
description: Dieses Cookbook enthält Informationen für Entwickler über Platt Formänderungen an den Windows 10-Betriebssystemen (OS).
ms.assetid: bf8d7d10-bab6-4711-b65f-5393d906e47b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03fce627969573deb395fda356564a85a3573682
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390858"
---
# <a name="windows-10"></a><span data-ttu-id="8ab18-103">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ab18-103">Windows 10</span></span>

<span data-ttu-id="8ab18-104">Dieses Cookbook enthält Informationen für Entwickler über Platt Formänderungen an den Windows 10-Betriebssystemen (OS).</span><span class="sxs-lookup"><span data-stu-id="8ab18-104">This Cookbook provides info for developers about platform changes to the Windows 10 operating systems (OS).</span></span> <span data-ttu-id="8ab18-105">Außerdem bieten wir Richtlinien für Sie, um die Kompatibilität Ihrer vorhandenen und geplanten apps mit der neuesten Version des Betriebssystems zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8ab18-105">We also provide guidelines for you to verify the compatibility of your existing and planned apps with the latest version of the OS.</span></span> <span data-ttu-id="8ab18-106">Wir gehen davon aus, dass Sie mit früheren Windows-Versionen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="8ab18-106">We assume that you are familiar with previous versions of Windows.</span></span>

<span data-ttu-id="8ab18-107">Der Inhalt gilt für: Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ab18-107">The content applies to: Windows 10</span></span>

<span data-ttu-id="8ab18-108">Das Cookbook eignet sich für Entwickler von apps und Geräten von Drittanbietern, die für die Verwendung in der Microsoft Windows-Umgebung entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="8ab18-108">The Cookbook is for third party developers of apps and devices that are designed to be used in the Microsoft Windows environment.</span></span>

## <a name="introduction"></a><span data-ttu-id="8ab18-109">Einführung</span><span class="sxs-lookup"><span data-stu-id="8ab18-109">Introduction</span></span>

<span data-ttu-id="8ab18-110">Windows 10 bietet die neuesten Betriebssystemtechnologien und softwareentwicklungsplattformen für die Verwendung durch APP-und Treiber Entwickler und Unternehmen auf der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="8ab18-110">Windows 10 introduces the latest OS technology and software development platforms for use by app and driver developers and enterprises worldwide.</span></span> <span data-ttu-id="8ab18-111">Um die Sicherheit, Zuverlässigkeit, Leistung und Benutzer Leistung von Windows weiter zu verbessern, hat Microsoft viele neue Features eingeführt, vorhandene Features verbessert und andere entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ab18-111">To further enhance the security, reliability, performance, and user experience of Windows, Microsoft has introduced many new features, improved existing features, and removed others.</span></span>

<span data-ttu-id="8ab18-112">Das Ziel von Windows 10 besteht darin, die Kompatibilität mit apps zu gewährleisten, die für zuvor veröffentlichte Versionen des Windows-Betriebssystems geschrieben wurden. einige Kompatibilitäts Umbrüche sind aufgrund von Innovationen, erhöhter Sicherheit und erhöhter Zuverlässigkeit unvermeidlich.</span><span class="sxs-lookup"><span data-stu-id="8ab18-112">While the goal of Windows 10 is to maintain compatibility with apps written for previously released versions of the Windows OS, some compatibility breaks are inevitable due to innovations, tightened security, and increased reliability.</span></span> <span data-ttu-id="8ab18-113">Insgesamt ist die Kompatibilität der neuesten Version des Windows-Betriebssystems mit vorhandenen apps und Geräten hoch.</span><span class="sxs-lookup"><span data-stu-id="8ab18-113">Overall, the compatibility of the latest version of the Windows OS with existing apps and devices is high.</span></span>

<span data-ttu-id="8ab18-114">In diesem Dokument erfahren Sie, wie Sie überprüfen, ob Ihre apps und Geräte mit der aktuellen Version des Betriebssystems kompatibel sind, und Sie erhalten eine Übersicht über bekannte Probleme bei der APP-Inkompatibilität.</span><span class="sxs-lookup"><span data-stu-id="8ab18-114">This document shows you how to verify that your apps and devices are compatible with the latest version of the OS and provides an overview of known app incompatibility issues.</span></span>

<span data-ttu-id="8ab18-115">Wir laden Sie in diese Themen ein, um zu erfahren, wie Sie Ihre apps optimieren und die Vorteile dieser neuesten Version von Windows nutzen können.</span><span class="sxs-lookup"><span data-stu-id="8ab18-115">We invite you to check out these topics to learn how to optimize your apps and take advantage of what this newest release of Windows has to offer.</span></span>

## <a name="contents"></a><span data-ttu-id="8ab18-116">Inhalte</span><span class="sxs-lookup"><span data-stu-id="8ab18-116">Contents</span></span>

-   [<span data-ttu-id="8ab18-117">Wichtige Änderungen seit Windows 7, um die Kompatibilität zu gewährleisten</span><span class="sxs-lookup"><span data-stu-id="8ab18-117">Key changes since Windows 7 to ensure compatibility</span></span>](key-changes-since-windows-7-to-ensure-compatibility.md)
-   [<span data-ttu-id="8ab18-118">Wie wir die Kompatibilität des kombinierten Ökosystems gewährleisten können</span><span class="sxs-lookup"><span data-stu-id="8ab18-118">How we can ensure compatibility of the combined ecosystem</span></span>](how-we-can-ensure-compatibility-of-the-combined-ecosystem.md)
    -   [<span data-ttu-id="8ab18-119">Windows-Versionsprüfung</span><span class="sxs-lookup"><span data-stu-id="8ab18-119">Windows version check</span></span>](windows-version-check.md)
    -   [<span data-ttu-id="8ab18-120">Nicht dokumentierte APIs</span><span class="sxs-lookup"><span data-stu-id="8ab18-120">Undocumented APIs</span></span>](undocumented-apis.md)
    -   [<span data-ttu-id="8ab18-121">Entwickeln von UWP-und Desktop Bridge-apps</span><span class="sxs-lookup"><span data-stu-id="8ab18-121">Develop UWP and Desktop Bridge apps</span></span>](/windows/desktop/w8cookbook/develop-universal-windows-platform-apps)
    -   [<span data-ttu-id="8ab18-122">Die Funktionalität der modernen Desktop-App ist beeinträchtigt, wenn Sie nicht im Fenstermodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ab18-122">Modern Desktop App functionality is impacted if not run in Windowed Mode</span></span>](modern-desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode.md)
    -   [<span data-ttu-id="8ab18-123">Verfügbarkeit der anwendbaren Grafiktreiber auf Windows Update</span><span class="sxs-lookup"><span data-stu-id="8ab18-123">Availability of applicable graphics drivers on Windows Update</span></span>](availability-of-applicable-graphics-drivers-on-windows-update.md)
    -   [<span data-ttu-id="8ab18-124">Migration von Grafiktreibern zu Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ab18-124">Graphics driver migration to Windows 10</span></span>](graphics-driver-migration-to-windows-10.md)
    -   [<span data-ttu-id="8ab18-125">Bluetooth-Treiber</span><span class="sxs-lookup"><span data-stu-id="8ab18-125">Bluetooth drivers</span></span>](bluetooth-drivers.md)

## <a name="download-the-cookbook"></a><span data-ttu-id="8ab18-126">Cookbook herunterladen</span><span class="sxs-lookup"><span data-stu-id="8ab18-126">Download the cookbook</span></span>

<span data-ttu-id="8ab18-127">Eine Kurzübersicht zu all diesen Informationen sowie Informationen zu Windows-as-a-Service, unterstützenden apps in Windows und optimierten Strategien zum Testen Ihrer App finden [Sie unter Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span><span class="sxs-lookup"><span data-stu-id="8ab18-127">For a quick reference to all this information, as well as information on Windows as a service, supporting apps in Windows, and optimized strategies for testing your app, [download the Windows 10 Compatibility Cookbook](https://download.microsoft.com/download/3/D/3/3D36E358-A7E4-4DA3-9FC4-6E85C850A6C6/Windows%2010%20Compatibility%20Cookbook.docx).</span></span>

## <a name="see-also"></a><span data-ttu-id="8ab18-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ab18-128">See Also</span></span>

-   <span data-ttu-id="8ab18-129">[Windows-as-a-Service](/windows/deployment/update/), Informationen zu Windows 10-releasetypen und app-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="8ab18-129">[Windows as a service](/windows/deployment/update/), for information about Windows 10 release types and app support.</span></span>
-   <span data-ttu-id="8ab18-130">[Windows-Insider](https://insider.windows.com/), um auf Preview-Builds zuzugreifen, zu testen und Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="8ab18-130">[Windows Insider](https://insider.windows.com/), to access preview builds, test, and provide feedback.</span></span>
-   <span data-ttu-id="8ab18-131">[Bereit für Windows 10](https://www.readyfor10.com/), um die Informationen Ihres Unternehmens an eine Ressource für IT-Manager zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="8ab18-131">[Ready for Windows 10](https://www.readyfor10.com/), to submit your company's information to a resource for IT managers.</span></span>

 

 