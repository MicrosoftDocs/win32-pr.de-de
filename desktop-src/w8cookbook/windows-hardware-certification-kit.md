---
title: Windows-Zertifizierungkit für Hardware
description: Windows-Zertifizierungkit für Hardware
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039737"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="9313e-103">Windows-Zertifizierungkit für Hardware</span><span class="sxs-lookup"><span data-stu-id="9313e-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="9313e-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="9313e-104">Platforms</span></span>

 <span data-ttu-id="9313e-105">**Clients** -Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="9313e-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="9313e-106">**Server** -Windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9313e-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="9313e-107">**Server/Controller** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9313e-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="9313e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9313e-108">Description</span></span>

<span data-ttu-id="9313e-109">Das Windows-hardwarezertifizierungskit ermöglicht Entwicklern, ISVs, IHVs und OEMs, Ihre Hardware Geräte, Systeme und Filtertreiber für die neuesten Windows-Betriebssysteme zu zertifizieren.</span><span class="sxs-lookup"><span data-stu-id="9313e-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="9313e-110">Sie enthält alle Tools und Dokumentationen, die Sie benötigen, um Ihre Hardware-und Filtertreiber für diese Betriebssysteme zu zertifizieren:</span><span class="sxs-lookup"><span data-stu-id="9313e-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="9313e-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9313e-111">Windows 8</span></span>
-   <span data-ttu-id="9313e-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9313e-112">Windows Server 2012</span></span>
-   <span data-ttu-id="9313e-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9313e-113">Windows 7</span></span>
-   <span data-ttu-id="9313e-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9313e-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="9313e-115">Das Windows-hardwarezertifizierungskit ersetzt das Windows-Logo-Kit und ist Bestandteil des Windows-Zertifizierungsprogramms.</span><span class="sxs-lookup"><span data-stu-id="9313e-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="9313e-116">Verwendung oder bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="9313e-116">Usage or best practices</span></span>

<span data-ttu-id="9313e-117">Bevor Sie Hardware-oder Filtertreiber testen können, müssen Sie die richtige Testumgebung basierend auf der Hardware oder dem Filtertreiber einrichten, die Sie zertifizieren.</span><span class="sxs-lookup"><span data-stu-id="9313e-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="9313e-118">Dies umfasst den Controller, den Client und möglicherweise zusätzliche Hardware (z. b. Geräte mit mehreren Funktionen) oder Software.</span><span class="sxs-lookup"><span data-stu-id="9313e-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="9313e-119">Nachdem Sie Ihre Umgebung eingerichtet haben, können Sie Ihre Hardware mit dem neuen HCK-Tool Studio testen.</span><span class="sxs-lookup"><span data-stu-id="9313e-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="9313e-120">Diese Schritte beschreiben den Zertifizierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="9313e-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="9313e-121">Einrichten der Testumgebung:</span><span class="sxs-lookup"><span data-stu-id="9313e-121">Set up test environment.</span></span>
2.  <span data-ttu-id="9313e-122">Erstellt ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="9313e-122">Create a project.</span></span>
3.  <span data-ttu-id="9313e-123">Erstellen Sie einen oder mehrere Computerpools.</span><span class="sxs-lookup"><span data-stu-id="9313e-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="9313e-124">Wählen Sie Features zum Überprüfen aus.</span><span class="sxs-lookup"><span data-stu-id="9313e-124">Select features to validate.</span></span>
5.  <span data-ttu-id="9313e-125">Wählen Sie Tests aus, und führen Sie diese aus.</span><span class="sxs-lookup"><span data-stu-id="9313e-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="9313e-126">Anzeigen der Testergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9313e-126">View test results.</span></span>
7.  <span data-ttu-id="9313e-127">Senden Sie Ihr Paket.</span><span class="sxs-lookup"><span data-stu-id="9313e-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="9313e-128">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9313e-128">Resources</span></span>

-   [<span data-ttu-id="9313e-129">Windows-Hardware Entwicklung</span><span class="sxs-lookup"><span data-stu-id="9313e-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="9313e-130">[Windows-Hardware Zertifizierungsprogramm](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9313e-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="9313e-131">[Einstieg in die Entwicklung von Hardware für Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9313e-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 