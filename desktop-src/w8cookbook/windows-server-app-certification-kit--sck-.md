---
title: MPR (Microsoft Platform Ready)-Testtool
description: MPR (Microsoft Platform Ready)-Testtool
ms.assetid: C41FBE70-E392-4FD0-954B-6C24168CB93E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6286e7ed64f013a8ea002ea392ba0d3bcac67296
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730728"
---
# <a name="microsoft-platform-ready-test-tool"></a><span data-ttu-id="ad09f-103">MPR (Microsoft Platform Ready)-Testtool</span><span class="sxs-lookup"><span data-stu-id="ad09f-103">Microsoft Platform Ready Test Tool</span></span>

## <a name="platform"></a><span data-ttu-id="ad09f-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="ad09f-104">Platform</span></span>

 <span data-ttu-id="ad09f-105">**Server** – Windows Server 2012 \| Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ad09f-105">**Servers** – Windows Server 2012 \| Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="ad09f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ad09f-106">Description</span></span>

<span data-ttu-id="ad09f-107">Das Microsoft Platform Ready (MPR)-Testtool wird für Platt Form Anwendungs Bereitschaft und zur Überprüfung der Konformität mit den Zertifizierungsanforderungen für Windows Server 2012-und Windows Server 2012 R2-Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad09f-107">The Microsoft Platform Ready (MPR) Test Tool is used for platform application readiness and to validate compliance with certification requirements for Windows Server 2012 and Windows Server 2012 R2 applications.</span></span>

<span data-ttu-id="ad09f-108">Microsoft ermutigt nachdrücklich, das MPR-Testtool in die Softwareverteilungs-und Test Prozesse einzubinden, um die Platt Form Bereitschaft sicherzustellen, bevor Anwendungen auf dem Markt veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="ad09f-108">Microsoft strongly encourages incorporating the MPR Test Tool into the software build and test processes, thereby ensuring platform readiness before applications are released to market.</span></span> <span data-ttu-id="ad09f-109">Das MPR-Testtool ist auch ein empfohlenes Tool zum Testen von Branchen Anwendungen und zum Auswerten von Server Produkten für Ihre Platt Form Kompatibilität, bevor Kaufentscheidungen getroffen werden.</span><span class="sxs-lookup"><span data-stu-id="ad09f-109">The MPR Test Tool is also a recommended tool to test line of business applications and for evaluating server products for their platform compatibility before making purchasing decisions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad09f-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad09f-110">Requirements</span></span>

<span data-ttu-id="ad09f-111">Das MPR-Testtool umfasst automatisierte Tests für:</span><span class="sxs-lookup"><span data-stu-id="ad09f-111">The MPR Test Tool includes automated tests for:</span></span>

-   <span data-ttu-id="ad09f-112">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="ad09f-112">Windows Installer</span></span>
-   <span data-ttu-id="ad09f-113">Setup und primäre Funktionalität</span><span class="sxs-lookup"><span data-stu-id="ad09f-113">Setup and Primary Functionality</span></span>
-   <span data-ttu-id="ad09f-114">Treiber und Sicherheit</span><span class="sxs-lookup"><span data-stu-id="ad09f-114">Drivers and Security</span></span>
-   <span data-ttu-id="ad09f-115">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="ad09f-115">Best Practices</span></span>

<span data-ttu-id="ad09f-116">Selbsttests und die Übermittlung von Ergebnissen für die meisten Server-apps sollten höchstens 2 Stunden dauern. komplexere Apps können ungefähr vier Stunden dauern.</span><span class="sxs-lookup"><span data-stu-id="ad09f-116">Self-testing and submission of results for most Server apps should take 2 hours or less; more complex apps can take around 4 hours.</span></span>

<span data-ttu-id="ad09f-117">Alle Treiber müssen die Windows-Hardware Zertifizierungsprüfung separat durchlaufen und von Microsoft für Windows Server 2012 signiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad09f-117">All drivers must separately pass Windows Hardware Certification testing and be signed by Microsoft for Windows Server 2012.</span></span>

## <a name="usage"></a><span data-ttu-id="ad09f-118">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="ad09f-118">Usage</span></span>

<span data-ttu-id="ad09f-119">So testen Sie Ihre apps:</span><span class="sxs-lookup"><span data-stu-id="ad09f-119">To test your apps:</span></span>

1.  <span data-ttu-id="ad09f-120">Installieren Sie die neueste Windows Server 2012-Mindestkonfiguration (vollständige Server-GUI, minimale Server Schnittstelle oder Server Core), wie Sie für Ihre APP erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ad09f-120">Install the latest Windows Server 2012 minimum configuration (Full Server GUI, Minimal Server Interface, or Server Core) as required for your app.</span></span>
2.  <span data-ttu-id="ad09f-121">Überprüfen Sie die Zertifizierungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="ad09f-121">Review the certification requirements.</span></span>
3.  <span data-ttu-id="ad09f-122">Führen Sie das MPR-Testtool auf einem sauberen System entweder im vollständigen oder im Befehlszeilen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="ad09f-122">On a clean system, run the MPR Test Tool in either full UI mode or command line mode.</span></span>
4.  <span data-ttu-id="ad09f-123">Schließen Sie den selbstgesteuerten Testprozess ab.</span><span class="sxs-lookup"><span data-stu-id="ad09f-123">Complete the self-guided testing process.</span></span>
5.  <span data-ttu-id="ad09f-124">Überprüfen Sie die Ergebnisse, und korrigieren Sie Ihre APP nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="ad09f-124">Review results and fix your app as required.</span></span>
6.  <span data-ttu-id="ad09f-125">Melden Sie sich an, und laden Sie erfolgreiche Ergebnisse in das Microsoft Platform Ready-Portal für die Auflistung im Windows Server-Katalog und die Verwendung des Logos hoch.</span><span class="sxs-lookup"><span data-stu-id="ad09f-125">Sign-in and upload successful results to Microsoft Platform Ready portal for listing in Windows Server Catalog and usage of the logo.</span></span>

## <a name="resources"></a><span data-ttu-id="ad09f-126">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ad09f-126">Resources</span></span>

-   [<span data-ttu-id="ad09f-127">Anforderungen an das Zertifizierungsprogramm für Windows Server-apps</span><span class="sxs-lookup"><span data-stu-id="ad09f-127">Requirements for Windows Server App Certification Program</span></span>](../win_cert/certification-requirements-for-windows-desktop-apps.md)
-   [<span data-ttu-id="ad09f-128">MPR-Testtool (Microsoft Platform Ready)</span><span class="sxs-lookup"><span data-stu-id="ad09f-128">Microsoft Platform Ready (MPR) Test Tool</span></span>](https://www.microsoft.com/download/details.aspx?id=37143)
-   [<span data-ttu-id="ad09f-129">Windows Server 2012-Anwendungs Zertifizierungsprogramm</span><span class="sxs-lookup"><span data-stu-id="ad09f-129">Windows Server 2012 Application Certification Program</span></span>](https://azure.microsoft.com/overview/commercial-marketplace/)
-   [<span data-ttu-id="ad09f-130">Feedback zum Windows Server-Logo</span><span class="sxs-lookup"><span data-stu-id="ad09f-130">Windows Server Logo Feedback</span></span>](mailto:WSLogoFB@microsoft.com)

 

 