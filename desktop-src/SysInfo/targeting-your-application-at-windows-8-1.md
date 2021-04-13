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
# <a name="targeting-your-application-for-windows"></a>Zielanwendung für Ihre Anwendung für Windows

In Windows 8.1 und Windows 10 wurden die Funktionen [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) und [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) als veraltet markiert. In Windows 10 wurde die Funktion " [**verifyversioninfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) " ebenfalls als veraltet markiert. Obwohl Sie die veralteten Funktionen weiterhin abrufen können, gibt die Funktion die Windows 8-Version (6,2) zurück, wenn die Anwendung nicht speziell Windows 8.1 oder Windows 10 als Ziel verwendet.

> [!Note]  
> Die Funktionen " [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion)", " [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)", " [**verifyversioninfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)" und " [Version Helper](version-helper-apis.md) " sind nur für Desktop-Apps vorgesehen. Universelle Windows-Apps können die [**analyticsinfo. VERSIONINFO**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) -Eigenschaft für Telemetriedaten und Diagnoseprotokolle verwenden.

Damit Ihre APP auf Windows 8.1 oder Windows 10 ausgerichtet ist, müssen Sie ein [App-Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP einschließen. Anschließend müssen Sie im [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests ein **&lt; SupportedOS &gt;** -Element für jede Windows-Version hinzufügen, die von ihrer App unterstützt wird.

Das folgende Beispiel zeigt eine APP-Manifest-Datei für eine APP, die alle Versionen von Windows von Windows Vista bis Windows 10 unterstützt:

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

Das Deklarieren der Unterstützung für Windows 8.1 oder Windows 10 in Ihrem App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.

Das obige App-Manifest enthält auch einen [ **&lt; Trust &gt; Info** -Abschnitt](/previous-versions/bb756929(v=msdn.10)), der angibt, wie das System es in Bezug auf die [Benutzerkontensteuerung (User Account Control, UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works)behandeln soll. Das Hinzufügen von **Trust Info** ist nicht zwingend erforderlich, aber es wird dringend empfohlen, auch wenn Ihre APP kein bestimmtes UAC-bezogenes Verhalten benötigt. Insbesondere, wenn Sie **trustInfo** überhaupt nicht hinzufügen, unterliegen die 32-Bit-x86-Versionen Ihrer APP der [UAC-Dateivirtualisierung](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), mit der Schreibvorgänge in Ordner mit Administratorrechten, wie z. b. die Windows-Systemordner, erfolgreich durchgeführt werden können, um Sie andernfalls zu einem benutzerspezifischen Ordner "virtualstore" zu leiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Version wird erhalten](getting-the-system-version.md)
</dt> <dt>

[Versions Hilfsfunktionen](version-helper-apis.md)
</dt> <dt>

[OSVersionInfo](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
