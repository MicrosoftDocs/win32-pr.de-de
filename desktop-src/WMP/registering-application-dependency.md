---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)
description: Anwendungs Abhängigkeit wird registriert
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, Registrierungs Einstellungen für Anwendungsabhängigkeiten
- Windows Media Player, Einstellungen für die Abhängigkeits Registrierung
- Windows Media Player, Registrierung
- Registrierung, Anwendungs Abhängigkeits Einstellungen
- Registrierung, Abhängigkeits Einstellungen
- Registrierung, Einstellungen für Windows-Media Player
- Abhängigkeits Registrierungs Einstellungen
- Registrierungs Einstellungen für Anwendungsabhängigkeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474985"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="51101-111">Registrieren von Anwendungsabhängigkeiten (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="51101-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="51101-112">Anwendungen, die vom Windows Media Player SDK oder Windows Media Format SDK bereitgestellte APIs verwenden, sind von den Laufzeitkomponenten dieser Technologien abhängig.</span><span class="sxs-lookup"><span data-stu-id="51101-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="51101-113">Sie können Ihre Anwendung im Rahmen des Anwendungs Setups als von diesen Komponenten abhängig registrieren.</span><span class="sxs-lookup"><span data-stu-id="51101-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="51101-114">Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeits Ebenen auswählen: "blockieren" oder "abhängig".</span><span class="sxs-lookup"><span data-stu-id="51101-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="51101-115">Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert sind, wird die Komponente von einem Rollback auf eine vorherige Version blockiert.</span><span class="sxs-lookup"><span data-stu-id="51101-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="51101-116">Abhängige Anwendungen, die nicht als Blockierung registriert sind, blockieren kein Rollback.</span><span class="sxs-lookup"><span data-stu-id="51101-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="51101-117">Stattdessen wird dem Benutzer vor der Ausführung des Rollbacks eine Meldung angezeigt, die besagt, dass die Anwendungen von der Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="51101-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="51101-118">Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51101-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="51101-119">Der festzulegende Registrierungs Wert hängt von der Komponente ab, von der die Anwendung abhängt.</span><span class="sxs-lookup"><span data-stu-id="51101-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="51101-120">Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51101-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="51101-121">Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der Windows Media Player SDK-Laufzeit zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="51101-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="51101-122">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"</span><span class="sxs-lookup"><span data-stu-id="51101-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="51101-123">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Descriptor, "*App*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="51101-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="51101-124">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMP \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="51101-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="51101-125">Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der SDK-Laufzeit des Windows Media-Formats zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="51101-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="51101-126">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Windows Media \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"</span><span class="sxs-lookup"><span data-stu-id="51101-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="51101-127">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup Referenz \\ *\_ Typdeskriptor* \\ , "*App*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="51101-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="51101-128">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="51101-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="51101-129">In den oben aufgeführten Registrierungs Werten werden die folgenden Variablen verwendet:</span><span class="sxs-lookup"><span data-stu-id="51101-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="51101-130">*\_Verweistyp*</span><span class="sxs-lookup"><span data-stu-id="51101-130">*REF\_TYPE*</span></span>

<span data-ttu-id="51101-131">Ersetzen Sie dies durch blockingref Counts zum Blockieren der Abhängigkeit oder durch dependentref Counts für nicht blockierende Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="51101-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="51101-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="51101-132">*APP*</span></span>

<span data-ttu-id="51101-133">Der Name oder der kurze Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="51101-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="51101-134">Diese Zeichenfolge wird nicht in Nachrichten verwendet, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51101-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="51101-135">Dieser Wert ist der Bezeichner, der in allen drei Registrierungs Werten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="51101-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="51101-136">*APP- \_ Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="51101-136">*APP\_STRING*</span></span>

<span data-ttu-id="51101-137">Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="51101-137">Descriptor of your application.</span></span> <span data-ttu-id="51101-138">Diese Zeichenfolge kann in Nachrichten verwendet werden, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51101-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="51101-139">*Verweis \_ Deskriptor*</span><span class="sxs-lookup"><span data-stu-id="51101-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="51101-140">Beschreibung der Verwendung der Komponente durch Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="51101-140">Description of how your application uses the component.</span></span> <span data-ttu-id="51101-141">Dieser Wert kann maximal 256 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="51101-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="51101-142">*WMP- \_ Version*</span><span class="sxs-lookup"><span data-stu-id="51101-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="51101-143">Die Version von Windows Media Player, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="51101-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="51101-144">Wenn keine Version angegeben wird, wird angenommen, dass es sich bei dem Standardwert um 9.0.0.0 handelt.</span><span class="sxs-lookup"><span data-stu-id="51101-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="51101-145">*WMF- \_ Version*</span><span class="sxs-lookup"><span data-stu-id="51101-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="51101-146">Die Version des Windows Media-SDK, das für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="51101-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="51101-147">Die folgenden drei Beispiel Registrierungs Werte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="51101-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="51101-148">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ app, "southridgevideo", "southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="51101-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="51101-149">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ Descriptor, "southridgevideo", "southridge Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Video Dateien".</span><span class="sxs-lookup"><span data-stu-id="51101-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="51101-150">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ dependentrefcounts \\ Version, "southridgevideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="51101-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="51101-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51101-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51101-152">**Registrierungs Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="51101-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




