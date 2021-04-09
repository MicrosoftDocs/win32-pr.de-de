---
title: Benutzeroberflächenautomatisierung
description: Microsoft UI Automation ist ein Barrierefreiheits Framework, mit dem Windows-Anwendungen programmgesteuerte Informationen zu Benutzeroberflächen (User Interface, UIs) bereitstellen und nutzen können.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858378"
---
# <a name="ui-automation"></a><span data-ttu-id="6e2a2-103">Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6e2a2-103">UI Automation</span></span>

<span data-ttu-id="6e2a2-104">Microsoft UI Automation ist ein Barrierefreiheits Framework, mit dem Windows-Anwendungen programmgesteuerte Informationen zu Benutzeroberflächen (User Interface, UIs) bereitstellen und nutzen können.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="6e2a2-105">Sie ermöglicht programmgesteuerten Zugriff auf die meisten Elemente der Benutzeroberfläche auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="6e2a2-106">Sie ermöglicht Hilfstechnologieprodukten, wie z. b. Bildschirm Sprachausgaben, Informationen zur Benutzeroberfläche für Endbenutzer bereitzustellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="6e2a2-107">Die Benutzeroberflächen Automatisierung ermöglicht außerdem die Interaktion von automatisierten Test Skripts mit der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="6e2a2-108">Ggf.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="6e2a2-109">Entwickler Zielgruppe</span><span class="sxs-lookup"><span data-stu-id="6e2a2-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="6e2a2-110">Lauf Zeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="6e2a2-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="6e2a2-111">Unterstützung für Betriebssysteme mit Unterstützung</span><span class="sxs-lookup"><span data-stu-id="6e2a2-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="6e2a2-112">Anwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="6e2a2-112">Where Applicable</span></span>

<span data-ttu-id="6e2a2-113">Durch die Verwendung der Benutzeroberflächen Automatisierung und der folgenden Barrierefreiheits Funktionen können Entwickler Anwendungen, die auf Windows ausgeführt werden, für viele Personen mit Sehbehinderung, Hörbehinderungen oder Bewegungsbehinderungen leichter zugänglich machen.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="6e2a2-114">Außerdem ist die Benutzeroberflächen Automatisierung speziell für die Bereitstellung robuster Funktionen für automatisierte Testszenarien konzipiert.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6e2a2-115">Entwicklerzielgruppe</span><span class="sxs-lookup"><span data-stu-id="6e2a2-115">Developer Audience</span></span>

<span data-ttu-id="6e2a2-116">Die Benutzeroberflächen Automatisierung wurde für erfahrene C/C++-Entwickler entwickelt.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="6e2a2-117">Im Allgemeinen benötigen Entwickler einen mittleren Einblick in die Component Object Model (com)-Objekte und-Schnittstellen, die Unicode-und die Windows-API-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="6e2a2-118">Weitere Informationen zur Benutzeroberflächen Automatisierung für verwalteten Code finden Sie im MSDN-Abschnitt .NET Framework Developer es Guide ( [Barrierefreiheit](/dotnet/framework/ui-automation/) ).</span><span class="sxs-lookup"><span data-stu-id="6e2a2-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6e2a2-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="6e2a2-119">Run-Time Requirements</span></span>

<span data-ttu-id="6e2a2-120">Die Automatisierung der Benutzeroberfläche wird unter den folgenden Betriebssystemen unterstützt: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 und Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="6e2a2-121">Windows XP und Windows Server 2003 benötigen auch Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="6e2a2-122">Unterstützung für Betriebssysteme mit Unterstützung</span><span class="sxs-lookup"><span data-stu-id="6e2a2-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="6e2a2-123">Das Platt Form Update für Windows Vista ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen sowohl auf Windows 7 als auch auf Betriebssysteme von Windows 7 als Ziel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="6e2a2-124">Das Platt Form Update für Windows Server 2008 ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen sowohl auf Windows Server 2008 R2 als auch auf frühere Versionen von Windows Server zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="6e2a2-125">Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="6e2a2-126">Anwendungen von Drittanbietern, die ein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 erfordern, können Windows Update erkennen, ob es installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="6e2a2-127">Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 unterstützen beide das gesamte Feature "Windows Automation API 3,0", das auf den folgenden Betriebssystemen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6e2a2-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="6e2a2-128">Windows XP (Englisch)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="6e2a2-129">Windows XP Home SP3 x86</span><span class="sxs-lookup"><span data-stu-id="6e2a2-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="6e2a2-130">Windows XP Professional SP3 x86</span><span class="sxs-lookup"><span data-stu-id="6e2a2-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="6e2a2-131">Windows Server 2003 SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="6e2a2-132">Windows Vista (Englisch)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="6e2a2-133">Starter SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="6e2a2-134">Home Premium SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="6e2a2-135">Business SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="6e2a2-136">Enterprise SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="6e2a2-137">Ultimate SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="6e2a2-138">Windows Server 2008 (Englisch)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="6e2a2-139">Windows Server 2008 SP2 (x86 und x64)</span><span class="sxs-lookup"><span data-stu-id="6e2a2-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="6e2a2-140">Weitere Informationen zu beiden Updates finden Sie unter [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="6e2a2-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e2a2-141">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6e2a2-141">In this section</span></span>

-   [<span data-ttu-id="6e2a2-142">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="6e2a2-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="6e2a2-143">Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter</span><span class="sxs-lookup"><span data-stu-id="6e2a2-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="6e2a2-144">Benutzeroberflächenautomatisierungs-Client Programmiererhandbuch</span><span class="sxs-lookup"><span data-stu-id="6e2a2-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="6e2a2-145">Verweis</span><span class="sxs-lookup"><span data-stu-id="6e2a2-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="6e2a2-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e2a2-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="6e2a2-147">Anhänge</span><span class="sxs-lookup"><span data-stu-id="6e2a2-147">Appendixes</span></span>](appendix-entry.md)

 

 