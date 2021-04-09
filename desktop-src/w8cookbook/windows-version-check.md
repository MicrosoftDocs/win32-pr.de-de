---
title: Windows-Versionsprüfung
description: Die Betriebssystemversion wurde mit dem Windows 10-Betriebssystem Release inkrementiert.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102491"
---
# <a name="windows-version-check"></a><span data-ttu-id="74b59-103">Windows-Versionsprüfung</span><span class="sxs-lookup"><span data-stu-id="74b59-103">Windows version check</span></span>

<span data-ttu-id="74b59-104">Die Betriebssystemversion wurde mit dem Windows 10-Betriebssystem Release inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="74b59-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="74b59-105">Dies bedeutet, dass die interne Versionsnummer für Windows 10 auch in 10,0 geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="74b59-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="74b59-106">Die Anwendungs- und Gerätekompatibilität nach einer Änderung der Betriebssystemversion aufrechtzuerhalten, war uns schon immer sehr wichtig.</span><span class="sxs-lookup"><span data-stu-id="74b59-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="74b59-107">Bei den meisten App-Kategorien (ohne Kernel Abhängigkeiten) wirkt sich die Änderung nicht negativ auf die APP-Funktionalität aus, und vorhandene apps funktionieren unter Windows 10 weiterhin einwandfrei.</span><span class="sxs-lookup"><span data-stu-id="74b59-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="74b59-108">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="74b59-108">Manifestations</span></span>

<span data-ttu-id="74b59-109">Inwieweit sich diese Änderung auswirkt, richtet sich nach der jeweiligen App.</span><span class="sxs-lookup"><span data-stu-id="74b59-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="74b59-110">Dies bedeutet, dass alle Apps, die die Betriebssystemversion überprüfen, eine höhere Versionsnummer erhalten, was sich wie folgt äußern kann:</span><span class="sxs-lookup"><span data-stu-id="74b59-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="74b59-111">Apps können von App-Installern u. U. nicht installiert werden und nicht starten.</span><span class="sxs-lookup"><span data-stu-id="74b59-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="74b59-112">Apps können instabil werden oder abstürzen.</span><span class="sxs-lookup"><span data-stu-id="74b59-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="74b59-113">Apps können Fehlermeldungen ausgeben, aber weiterhin ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="74b59-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="74b59-114">Einige Apps überprüfen die Version und geben einfach eine Warnung an den Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="74b59-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="74b59-115">Es gibt jedoch auch Apps, für die eine Versionsprüfung unumgänglich ist (in den Treibern oder im Kernelmodus, um eine Erkennung zu vermeiden).</span><span class="sxs-lookup"><span data-stu-id="74b59-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="74b59-116">In diesen Fällen verursacht die App beim Auffinden einer falschen Version einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="74b59-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="74b59-117">Wir empfehlen statt einer Versionsprüfung eines der folgenden Verfahren:</span><span class="sxs-lookup"><span data-stu-id="74b59-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="74b59-118">Wenn die App von bestimmten API-Funktionen abhängig ist, stellen Sie sicher, dass sie auf die richtige API-Version ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="74b59-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="74b59-119">Die Versionsnummer von ntddi (NT-Gerätetreiber Schnittstelle) wird nur erhöht, wenn sich die Ziel Funktionalität in der API ändert.</span><span class="sxs-lookup"><span data-stu-id="74b59-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="74b59-120">Stellen Sie sicher, dass Sie die Änderung mithilfe von apiset oder einer anderen verfügbar gemachten API erkennen, wie Sie vom Featureteam erstellt wurde, und verwenden Sie die Version nicht als Proxy für ein Feature oder eine Korrektur.</span><span class="sxs-lookup"><span data-stu-id="74b59-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="74b59-121">Wenn für bedeutende Änderungen keine ordnungsgemäße Prüfung verfügbar gemacht wird, liegt ein Fehler vor.</span><span class="sxs-lookup"><span data-stu-id="74b59-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="74b59-122">Stellen Sie sicher, dass die APP nicht auf ungerade Weise auf eine Version prüft, wie z. b. über die Registrierung, Dateiversionen, Offsets, Kernel Modus, Treiber oder andere Mittel.</span><span class="sxs-lookup"><span data-stu-id="74b59-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="74b59-123">Wenn die APP unbedingt die Version überprüfen muss, verwenden Sie die GetVersion-APIs, die die Haupt-, neben-und Buildnummer zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="74b59-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="74b59-124">Wenn Sie die GetVersion-API oder andere Versions Hilfsobjekte wie [verifyversioninfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)verwenden, denken Sie daran, dass sich das Verhalten dieser API beginnend mit Windows 8.1 geändert hat.</span><span class="sxs-lookup"><span data-stu-id="74b59-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="74b59-125">Weitere Informationen finden Sie in [der API-Dokumentation](../SysInfo/version-helper-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="74b59-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="74b59-126">Wenn Sie apps wie Antischadsoftware oder Firewall besitzen, sollten Sie über ihre üblichen Feedback Kanäle und über das Windows Insider-Programm arbeiten.</span><span class="sxs-lookup"><span data-stu-id="74b59-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="74b59-127">Deklarieren der Windows 10-Kompatibilität mit einem App-Manifest</span><span class="sxs-lookup"><span data-stu-id="74b59-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="74b59-128">Wenn Ihre APP mit Windows 10 kompatibel ist, kann Sie diese Tatsache im APP- [Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP deklarieren.</span><span class="sxs-lookup"><span data-stu-id="74b59-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="74b59-129">Dadurch wird dem System mitgeteilt, dass Ihre APP die System Versionsnummer 10,0 von Windows 10 versteht (sodass die GetVersion-API keine frühere Version zurückgibt). Außerdem kann das System andere Kompatibilitäts Verhalten deaktivieren, die auf apps angewendet werden, die keine Windows 10-Kompatibilität deklarieren.</span><span class="sxs-lookup"><span data-stu-id="74b59-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="74b59-130">Um die Windows 10-Kompatibilität in einem App-Manifest zu deklarieren, müssen Sie einen [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests hinzufügen, sofern noch nicht vorhanden. Fügen Sie dann **&lt; SupportedOS &gt;** -Elemente für Windows 10 und jede andere Windows-Version hinzu, die von ihrer App unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="74b59-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="74b59-131">Das folgende Beispiel zeigt eine APP-Manifest-Datei für eine APP, die alle Versionen von Windows von Windows Vista bis Windows 10 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="74b59-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
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

<span data-ttu-id="74b59-132">Die oben markierte Zeile `* ADD THIS LINE *` zeigt, wie Sie Ihre Anwendung für Windows 10 genau ausrichten können.</span><span class="sxs-lookup"><span data-stu-id="74b59-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="74b59-133">Das Deklarieren der Unterstützung für Windows 10 in Ihrem App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.</span><span class="sxs-lookup"><span data-stu-id="74b59-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="74b59-134">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74b59-134">Resources</span></span>

-   [<span data-ttu-id="74b59-135">Download des Anwendungskompatibilitäts-Toolkits: Herunterladen des Windows ADK für Windows 10</span><span class="sxs-lookup"><span data-stu-id="74b59-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="74b59-136">[Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="74b59-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="74b59-137">API für Versions Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="74b59-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)