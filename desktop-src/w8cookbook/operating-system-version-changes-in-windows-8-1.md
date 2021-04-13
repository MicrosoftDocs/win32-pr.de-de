---
title: Änderungen an der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2
description: Änderungen an der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390936"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="a2e68-103">Änderungen an der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2e68-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="a2e68-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="a2e68-104">Platforms</span></span>

<span data-ttu-id="a2e68-105">**Clients:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a2e68-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="a2e68-106">**Server:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a2e68-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="a2e68-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a2e68-107">Description</span></span>

<span data-ttu-id="a2e68-108">Wir haben einige bedeutende Änderungen an der Funktionsweise der GetVersion (ex)-APIs in Windows 8.1 durchgeführt, weil unerwünschte Kunden Verhaltensweisen, die sich aus der Verwendung der GetVersion (ex)-APIs in der Vergangenheit ergeben haben.</span><span class="sxs-lookup"><span data-stu-id="a2e68-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="a2e68-109">In früheren Versionen von Windows gab das Aufrufen der GetVersion (ex)-APIs die tatsächliche Version des Betriebssystems (OS) zurück, es sei denn, der Prozess wurde durch eine APP Kompatibilitäts Shim verringert, um eine andere Version zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a2e68-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="a2e68-110">Dies wurde vorläufig durchgeführt und war relativ unvollständig in Bezug auf die Anzahl der Prozesse, die Microsoft in einem Release in gewisser Weise verarbeitbaren.</span><span class="sxs-lookup"><span data-stu-id="a2e68-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="a2e68-111">Viele Anwendungen haben die Risse durchlaufen, da Sie aufgrund von unzureichend entworfenen Versions Überprüfungen nicht geshimmt wurden.</span><span class="sxs-lookup"><span data-stu-id="a2e68-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="a2e68-112">Der einzige Grund, eine Versions Überprüfung durchzuführen, besteht darin, den Benutzer zu warnen, dass die Anwendung auf einer neueren Version des Betriebssystems ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a2e68-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="a2e68-113">Aufgrund von schlechten Überprüfungen würden apps jedoch häufig fälschlicherweise gewarnt, dass Sie unter Windows XP oder höher ausgeführt werden müssen, was natürlich das neueste Betriebssystem ist.</span><span class="sxs-lookup"><span data-stu-id="a2e68-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="a2e68-114">Meistens führt das neueste Betriebssystem die Anwendung ohne Probleme aus, wenn dies nicht für diese Überprüfungen der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="a2e68-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a2e68-115">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="a2e68-115">Manifestation</span></span>

<span data-ttu-id="a2e68-116">In Windows 8.1 wurden die GetVersion (ex)-APIs als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="a2e68-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="a2e68-117">Dies bedeutet, dass Sie die Windows 8-Version (6,2) zurückgeben können, während Sie diese API-Funktionen weiterhin abrufen können, wenn Ihre APP nicht speziell auf Windows 8.1 ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a2e68-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="a2e68-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="a2e68-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="a2e68-119">Hinzufügen eines App-Manifests</span><span class="sxs-lookup"><span data-stu-id="a2e68-119">Adding an app manifest</span></span>

<span data-ttu-id="a2e68-120">Damit Ihre APP auf Windows 8.1 abzielen kann, müssen Sie ein [App-Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP einschließen.</span><span class="sxs-lookup"><span data-stu-id="a2e68-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="a2e68-121">Anschließend müssen Sie im [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests ein **&lt; SupportedOS &gt;** -Element für jede Windows-Version hinzufügen, die von ihrer App unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a2e68-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="a2e68-122">Das folgende Beispiel zeigt eine APP-Manifest-Datei für eine APP, die alle Versionen von Windows von Windows Vista bis Windows 8.1 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a2e68-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

<span data-ttu-id="a2e68-123">Die oben markierte Zeile `* ADD THIS LINE *` zeigt, wie Sie Ihre Anwendung für Windows 8.1 genau ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="a2e68-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="a2e68-124">Das Deklarieren der Unterstützung für Windows 8.1 im App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2e68-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="a2e68-125">Verwenden von versionhilfsprogramme anstelle von GetVersion (ex)</span><span class="sxs-lookup"><span data-stu-id="a2e68-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="a2e68-126">Windows 8.1 führt neue Ersetzungs-API-Funktionen für GetVersion (ex) ein, die als versionhilfsprogramme bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a2e68-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="a2e68-127">Sie sind äußerst einfach zu verwenden. alles, was Sie tun müssen `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="a2e68-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="a2e68-128">Mit den Inline Funktionen, die in der Header Datei "versionhilfsprogramme. h" verfügbar sind, kann Ihr Code Fragen, ob das Betriebssystem eine bestimmte Version von Windows oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="a2e68-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="a2e68-129">**Beispiel** Wenn Ihre Anwendung z. b. Windows 8 oder höher erfordert, verwenden Sie den folgenden Test:</span><span class="sxs-lookup"><span data-stu-id="a2e68-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="a2e68-130">Die folgenden versionhelper-API-Funktionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="a2e68-130">The available VersionHelper API functions are:</span></span>

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

<span data-ttu-id="a2e68-131">Abhängig von der Frage, die Sie anfordern, wird "true" oder "false" zurückgegeben, und Sie müssen nur das Betriebssystem auf Mindestebene definieren, das Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a2e68-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="a2e68-132">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a2e68-132">Resources</span></span>

-   [<span data-ttu-id="a2e68-133">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="a2e68-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="a2e68-134">[Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a2e68-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="a2e68-135">Versionhilfsprogramme-APIs</span><span class="sxs-lookup"><span data-stu-id="a2e68-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)