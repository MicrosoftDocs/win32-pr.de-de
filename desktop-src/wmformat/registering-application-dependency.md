---
title: Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)
description: Anwendungs Abhängigkeit wird registriert
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media-Format-SDK, Registrieren von Anwendungsabhängigkeiten
- Anwendungsabhängigkeiten werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039914"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="4a781-105">Registrieren von Anwendungsabhängigkeiten (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="4a781-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4a781-106">Anwendungen, die APIs verwenden, die vom Windows Media-Format-SDK oder Windows Media Player SDK bereitgestellt werden, sind von den Laufzeitkomponenten dieser Technologien abhängig.</span><span class="sxs-lookup"><span data-stu-id="4a781-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="4a781-107">Sie können Ihre Anwendung im Rahmen des Anwendungs Setups als von diesen Komponenten abhängig registrieren.</span><span class="sxs-lookup"><span data-stu-id="4a781-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="4a781-108">Wenn Sie Ihre Anwendung registrieren, können Sie eine von zwei Abhängigkeits Ebenen auswählen: "blockieren" oder "abhängig".</span><span class="sxs-lookup"><span data-stu-id="4a781-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="4a781-109">Wenn eine oder mehrere Anwendungen mit einer blockierenden Abhängigkeit von einer der Laufzeitkomponenten registriert werden, wird die Komponente von einem Rollback auf eine vorherige Version blockiert.</span><span class="sxs-lookup"><span data-stu-id="4a781-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="4a781-110">Abhängige Anwendungen, die nicht als Blockierung registriert sind, blockieren kein Rollback.</span><span class="sxs-lookup"><span data-stu-id="4a781-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="4a781-111">Stattdessen wird der Benutzer vor dem Rollback aufgefordert, eine Meldung anzugeben, dass die Anwendungen von der Komponente abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="4a781-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="4a781-112">Um Ihre Anwendung zu registrieren, müssen Sie einen Wert in der Registrierung festlegen, der Ihre Anwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a781-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="4a781-113">Der festzulegende Registrierungs Wert hängt von der Komponente ab, von der die Anwendung abhängt.</span><span class="sxs-lookup"><span data-stu-id="4a781-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="4a781-114">Sie können auch zwei zusätzliche Werte pro Abhängigkeit festlegen, um zusätzliche Informationen zu Ihrer Anwendung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4a781-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="4a781-115">Die folgenden Registrierungs Werte werden verwendet, um die Abhängigkeit von der SDK-Laufzeit des Windows Media-Formats zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="4a781-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="4a781-116">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Windows Media \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"</span><span class="sxs-lookup"><span data-stu-id="4a781-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="4a781-117">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup Referenz \\ *\_ Typdeskriptor* \\ , "*App*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="4a781-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="4a781-118">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMF \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="4a781-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="4a781-119">Der folgende Registrierungs Wert wird verwendet, um die Abhängigkeit von der Windows Media Player SDK-Laufzeit zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="4a781-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="4a781-120">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ app, "*App*", "*App \_ String*"</span><span class="sxs-lookup"><span data-stu-id="4a781-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="4a781-121">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Descriptor, "*App*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="4a781-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="4a781-122">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ Media Player \\ Setup \\ *ref \_ Type* \\ Version, "*App*", "*WMP \_ Version*"</span><span class="sxs-lookup"><span data-stu-id="4a781-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="4a781-123">In den oben aufgeführten Registrierungs Werten werden die folgenden Variablen verwendet:</span><span class="sxs-lookup"><span data-stu-id="4a781-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="4a781-124">*\_Verweistyp*</span><span class="sxs-lookup"><span data-stu-id="4a781-124">*REF\_TYPE*</span></span>

<span data-ttu-id="4a781-125">Ersetzen Sie dies durch blockingref Counts zum Blockieren der Abhängigkeit oder durch dependentref Counts für nicht blockierende Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="4a781-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="4a781-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="4a781-126">*APP*</span></span>

<span data-ttu-id="4a781-127">Der Name oder der kurze Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4a781-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="4a781-128">Diese Zeichenfolge wird nicht in Nachrichten verwendet, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a781-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="4a781-129">Dieser Wert ist der Bezeichner, der in allen drei Registrierungs Werten verwendet wird, die den einzelnen Laufzeitkomponenten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4a781-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="4a781-130">*APP- \_ Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="4a781-130">*APP\_STRING*</span></span>

<span data-ttu-id="4a781-131">Deskriptor Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4a781-131">Descriptor of your application.</span></span> <span data-ttu-id="4a781-132">Diese Zeichenfolge kann in Nachrichten verwendet werden, die für den Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a781-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="4a781-133">*Verweis \_ Deskriptor*</span><span class="sxs-lookup"><span data-stu-id="4a781-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="4a781-134">Beschreibung der Verwendung der Komponente durch Ihre Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4a781-134">Description of how your application uses the component.</span></span> <span data-ttu-id="4a781-135">Dieser Wert kann maximal 256 Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="4a781-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="4a781-136">*WMP- \_ Version*</span><span class="sxs-lookup"><span data-stu-id="4a781-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="4a781-137">Die Version von Windows Media Player, die für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4a781-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="4a781-138">*WMF- \_ Version*</span><span class="sxs-lookup"><span data-stu-id="4a781-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="4a781-139">Die Version des Windows Media-SDK, das für Ihre Anwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4a781-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="4a781-140">Die folgenden drei Beispiel Registrierungs Werte veranschaulichen, wie die Werte für Ihre Anwendung konfiguriert werden:</span><span class="sxs-lookup"><span data-stu-id="4a781-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="4a781-141">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ dependentrefcounts \\ app, "southridgevideo", "southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="4a781-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="4a781-142">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ \\ Windows Media Setup \\ dependentrefcounts \\ Descriptor, "southridgevideo", "southridge Video Player verwendet das Windows Media Format SDK zum Wiedergeben von Video Dateien".</span><span class="sxs-lookup"><span data-stu-id="4a781-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="4a781-143">HKEY \_ Classes \_ root \\ Software \\ Microsoft \\ WindowsMedia \\ Setup \\ dependentrefcounts \\ Version, "southridgevideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="4a781-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a781-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a781-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a781-145">**Überlegungen zu Projekten**</span><span class="sxs-lookup"><span data-stu-id="4a781-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




