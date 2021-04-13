---
description: In Windows 8.1 und Windows 10 wurden die Funktionen GetVersion und GetVersionEx als veraltet markiert.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Zielanwendung für Ihre Anwendung für Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348458"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="38ce0-103">Zielanwendung für Ihre Anwendung für Windows</span><span class="sxs-lookup"><span data-stu-id="38ce0-103">Targeting your application for Windows</span></span>

<span data-ttu-id="38ce0-104">In Windows 8.1 und Windows 10 wurden die Funktionen [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) und [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="38ce0-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="38ce0-105">In Windows 10 wurde die Funktion " [**verifyversioninfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) " ebenfalls als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="38ce0-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="38ce0-106">Obwohl Sie die veralteten Funktionen weiterhin abrufen können, gibt die Funktion die Windows 8-Version (6,2) zurück, wenn die Anwendung nicht speziell Windows 8.1 oder Windows 10 als Ziel verwendet.</span><span class="sxs-lookup"><span data-stu-id="38ce0-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="38ce0-107">Die Funktionen " [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion)", " [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)", " [**verifyversioninfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)" und " [Version Helper](version-helper-apis.md) " sind nur für Desktop-Apps vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="38ce0-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="38ce0-108">Universelle Windows-Apps können die [**analyticsinfo. VERSIONINFO**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) -Eigenschaft für Telemetriedaten und Diagnoseprotokolle verwenden.</span><span class="sxs-lookup"><span data-stu-id="38ce0-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="38ce0-109">Damit Ihre APP auf Windows 8.1 oder Windows 10 ausgerichtet ist, müssen Sie ein [App-Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP einschließen.</span><span class="sxs-lookup"><span data-stu-id="38ce0-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="38ce0-110">Anschließend müssen Sie im [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests ein **&lt; SupportedOS &gt;** -Element für jede Windows-Version hinzufügen, die von ihrer App unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="38ce0-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="38ce0-111">Das folgende Beispiel zeigt eine APP-Manifest-Datei für eine APP, die alle Versionen von Windows von Windows Vista bis Windows 10 unterstützt:</span><span class="sxs-lookup"><span data-stu-id="38ce0-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
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
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

<span data-ttu-id="38ce0-112">Das Deklarieren der Unterstützung für Windows 8.1 oder Windows 10 in Ihrem App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.</span><span class="sxs-lookup"><span data-stu-id="38ce0-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="38ce0-113">Das obige App-Manifest enthält auch einen [ **&lt; Trust &gt; Info** -Abschnitt](/previous-versions/bb756929(v=msdn.10)), der angibt, wie das System es in Bezug auf die [Benutzerkontensteuerung (User Account Control, UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works)behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="38ce0-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="38ce0-114">Das Hinzufügen von **Trust Info** ist nicht zwingend erforderlich, aber es wird dringend empfohlen, auch wenn Ihre APP kein bestimmtes UAC-bezogenes Verhalten benötigt.</span><span class="sxs-lookup"><span data-stu-id="38ce0-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="38ce0-115">Insbesondere, wenn Sie **trustInfo** überhaupt nicht hinzufügen, unterliegen die 32-Bit-x86-Versionen Ihrer APP der [UAC-Dateivirtualisierung](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), mit der Schreibvorgänge in Ordner mit Administratorrechten, wie z. b. die Windows-Systemordner, erfolgreich durchgeführt werden können, um Sie andernfalls zu einem benutzerspezifischen Ordner "virtualstore" zu leiten.</span><span class="sxs-lookup"><span data-stu-id="38ce0-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38ce0-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38ce0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38ce0-117">System Version wird erhalten</span><span class="sxs-lookup"><span data-stu-id="38ce0-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="38ce0-118">Versions Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="38ce0-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="38ce0-119">OSVersionInfo</span><span class="sxs-lookup"><span data-stu-id="38ce0-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="38ce0-120">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="38ce0-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
