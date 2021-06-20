---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung mit Laufzeitkomponenten von APIs registrieren, die vom Windows Media Format 11 SDK bereitgestellt werden.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, Registrieren von Anwendungsabhängigkeiten
- Registrieren von Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406163"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="3127a-105">Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="3127a-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="3127a-106">Anwendungen, die APIs verwenden, die vom Windows Media Format SDK oder Windows Media Player SDK bereitgestellt werden, sind von den Laufzeitkomponenten dieser Technologien abhängig.</span><span class="sxs-lookup"><span data-stu-id="3127a-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="3127a-107">Sie können Ihre Anwendung im Rahmen der Anwendungseinrichtung als abhängig von diesen Komponenten registrieren.</span><span class="sxs-lookup"><span data-stu-id="3127a-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="3127a-108">Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig.</span><span class="sxs-lookup"><span data-stu-id="3127a-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="3127a-109">Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine frühere Version blockiert.</span><span class="sxs-lookup"><span data-stu-id="3127a-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="3127a-110">Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback.</span><span class="sxs-lookup"><span data-stu-id="3127a-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="3127a-111">Stattdessen wird der Benutzer vor dem Ausführen des Rollbacks mit einer Meldung aufgefordert, dass Anwendungen von der Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="3127a-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="3127a-112">Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3127a-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="3127a-113">Der registrierungswert, der festgelegt werden soll, hängt von der Komponente ab, von der Ihre Anwendung abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3127a-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="3127a-114">Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="3127a-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="3127a-115">Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von der Windows Media Format SDK-Runtime zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="3127a-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="3127a-116">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="3127a-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="3127a-117">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="3127a-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="3127a-118">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="3127a-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="3127a-119">Der folgende Registrierungswert wird verwendet, um die Abhängigkeit von Windows Media Player SDK-Runtime zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="3127a-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="3127a-120">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="3127a-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="3127a-121">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="3127a-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="3127a-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="3127a-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="3127a-123">Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:</span><span class="sxs-lookup"><span data-stu-id="3127a-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="3127a-124">*REF \_ TYPE*</span><span class="sxs-lookup"><span data-stu-id="3127a-124">*REF\_TYPE*</span></span>

<span data-ttu-id="3127a-125">Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="3127a-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="3127a-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="3127a-126">*APP*</span></span>

<span data-ttu-id="3127a-127">Der Name oder kurze Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3127a-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="3127a-128">Diese Zeichenfolge wird nicht in Meldungen verwendet, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3127a-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="3127a-129">Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3127a-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="3127a-130">*\_APP-ZEICHENFOLGE*</span><span class="sxs-lookup"><span data-stu-id="3127a-130">*APP\_STRING*</span></span>

<span data-ttu-id="3127a-131">Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3127a-131">Descriptor of your application.</span></span> <span data-ttu-id="3127a-132">Diese Zeichenfolge kann in Meldungen verwendet werden, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3127a-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="3127a-133">*\_REF-DESKRIPTOR*</span><span class="sxs-lookup"><span data-stu-id="3127a-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="3127a-134">Beschreibung der Verwendung der Komponente durch Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="3127a-134">Description of how your application uses the component.</span></span> <span data-ttu-id="3127a-135">Dieser Wert kann maximal 256 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="3127a-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="3127a-136">*\_WMP-VERSION*</span><span class="sxs-lookup"><span data-stu-id="3127a-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="3127a-137">Version der Windows Media Player, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3127a-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="3127a-138">*\_WMF-VERSION*</span><span class="sxs-lookup"><span data-stu-id="3127a-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="3127a-139">Version des Windows Media Format SDK, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3127a-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="3127a-140">Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="3127a-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="3127a-141">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "South southplayer"</span><span class="sxs-lookup"><span data-stu-id="3127a-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="3127a-142">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "South betriebssystemVideo", "South javascript Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="3127a-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="3127a-143">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="3127a-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="3127a-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3127a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3127a-145">**Überlegungen zum Projekt**</span><span class="sxs-lookup"><span data-stu-id="3127a-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




