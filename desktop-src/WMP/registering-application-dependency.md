---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)
description: Erfahren Sie, wie Sie Ihre Anwendung mit Laufzeitkomponenten von APIs registrieren, die vom Windows Media Player SDK bereitgestellt werden.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,Anwendungsabhängigkeitsregistrierungseinstellungen
- Windows Media Player,Einstellungen für die Abhängigkeitsregistrierung
- Windows Media Player,Registrierung
- Registrierung, Anwendungsabhängigkeitseinstellungen
- Registrierung, Abhängigkeitseinstellungen
- registry,settings for Windows Media Player
- Einstellungen für die Abhängigkeitsregistrierung
- Registrierungseinstellungen für Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407363"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="20ab2-111">Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="20ab2-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="20ab2-112">Anwendungen, die vom Windows Media Player SDK oder Windows Media Format SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig.</span><span class="sxs-lookup"><span data-stu-id="20ab2-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="20ab2-113">Sie können Ihre Anwendung im Rahmen der Anwendungseinrichtung als abhängig von diesen Komponenten registrieren.</span><span class="sxs-lookup"><span data-stu-id="20ab2-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="20ab2-114">Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeitsebenen auswählen: blockierend oder abhängig.</span><span class="sxs-lookup"><span data-stu-id="20ab2-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="20ab2-115">Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert sind, wird die Komponente von einem Rollback auf eine frühere Version blockiert.</span><span class="sxs-lookup"><span data-stu-id="20ab2-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="20ab2-116">Abhängige Anwendungen, die nicht als blockierend registriert sind, blockieren kein Rollback.</span><span class="sxs-lookup"><span data-stu-id="20ab2-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="20ab2-117">Stattdessen wird dem Benutzer vor dem Rollback eine Meldung angezeigt, die besagt, dass Anwendungen von der Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="20ab2-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="20ab2-118">Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="20ab2-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="20ab2-119">Der registrierungswert, der festgelegt werden soll, hängt von der Komponente ab, von der Ihre Anwendung abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="20ab2-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="20ab2-120">Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="20ab2-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="20ab2-121">Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von Windows Media Player SDK-Runtime zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="20ab2-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="20ab2-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="20ab2-123">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="20ab2-124">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="20ab2-125">Die folgenden Registrierungswerte werden verwendet, um die Abhängigkeit von der Windows Media Format SDK-Runtime zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="20ab2-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="20ab2-126">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="20ab2-127">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descriptor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="20ab2-128">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="20ab2-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="20ab2-129">Die folgenden Variablen werden in den oben aufgeführten Registrierungswerten verwendet:</span><span class="sxs-lookup"><span data-stu-id="20ab2-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="20ab2-130">*\_REF-TYP*</span><span class="sxs-lookup"><span data-stu-id="20ab2-130">*REF\_TYPE*</span></span>

<span data-ttu-id="20ab2-131">Ersetzen Sie durch BlockingRefCounts für blockierende Abhängigkeiten oder durch DependentRefCounts für nicht blockierende Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="20ab2-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="20ab2-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="20ab2-132">*APP*</span></span>

<span data-ttu-id="20ab2-133">Der Name oder kurze Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="20ab2-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="20ab2-134">Diese Zeichenfolge wird nicht in Meldungen verwendet, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="20ab2-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="20ab2-135">Dieser Wert ist der Bezeichner, der in allen drei Registrierungswerten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="20ab2-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="20ab2-136">*\_APP-ZEICHENFOLGE*</span><span class="sxs-lookup"><span data-stu-id="20ab2-136">*APP\_STRING*</span></span>

<span data-ttu-id="20ab2-137">Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="20ab2-137">Descriptor of your application.</span></span> <span data-ttu-id="20ab2-138">Diese Zeichenfolge kann in Meldungen verwendet werden, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="20ab2-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="20ab2-139">*\_REF-DESKRIPTOR*</span><span class="sxs-lookup"><span data-stu-id="20ab2-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="20ab2-140">Beschreibung der Verwendung der Komponente durch Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="20ab2-140">Description of how your application uses the component.</span></span> <span data-ttu-id="20ab2-141">Dieser Wert kann maximal 256 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="20ab2-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="20ab2-142">*\_WMP-VERSION*</span><span class="sxs-lookup"><span data-stu-id="20ab2-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="20ab2-143">Version der Windows Media Player, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="20ab2-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="20ab2-144">Wenn keine Version angegeben wird, wird als Standardwert 9.0.0.0 angenommen.</span><span class="sxs-lookup"><span data-stu-id="20ab2-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="20ab2-145">*\_WMF-VERSION*</span><span class="sxs-lookup"><span data-stu-id="20ab2-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="20ab2-146">Version des Windows Media Format SDK, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="20ab2-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="20ab2-147">Die folgenden drei Beispielregistrierungswerte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="20ab2-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="20ab2-148">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ App, "Southvideo", "Southuda Video Player"</span><span class="sxs-lookup"><span data-stu-id="20ab2-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="20ab2-149">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Descriptor, "South skriptvideo", "South javascript Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="20ab2-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="20ab2-150">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer Setup \\ \\ DependentRefCounts \\ Version, "Southvideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="20ab2-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="20ab2-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20ab2-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ab2-152">**Registrierungseinstellungen**</span><span class="sxs-lookup"><span data-stu-id="20ab2-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




