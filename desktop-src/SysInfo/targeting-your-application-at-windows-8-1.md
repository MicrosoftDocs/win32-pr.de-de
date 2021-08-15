---
description: In Windows 8.1 und Windows 10 sind die Funktionen GetVersion und GetVersionEx veraltet.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Ziel ihrer Anwendung für Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763111"
---
# <a name="targeting-your-application-for-windows"></a>Ziel ihrer Anwendung für Windows

In Windows 8.1 und Windows 10 sind [**die Funktionen GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) und [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) veraltet. In Windows 10 ist die [**VerifyVersionInfo-Funktion**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) ebenfalls veraltet. Sie können zwar weiterhin die veralteten Funktionen aufrufen, aber wenn Ihre Anwendung nicht speziell auf Windows 8.1 oder Windows 10 zielt, geben die Funktionen die Windows 8-Version (6.2) zurück.

> [!Note]  
> [**GetVersion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) [**GetVersionEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)und die [Versionshilfefunktionen](version-helper-apis.md) gelten nur für Desktop-Apps. Universelle Windows-Apps können die [**AnalyticsInfo.VersionInfo-Eigenschaft**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) für Telemetrie- und Diagnoseprotokolle verwenden.

Damit Ihre App auf Windows 8.1 oder Windows 10, müssen Sie ein [App-Manifest (ausführbares Manifest)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der App enthalten. Anschließend müssen Sie [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) im Kompatibilitätsabschnitt des Manifests ein **&lt; supportedOS-Element &gt;** für jede Windows-Version hinzufügen, die Sie deklarieren möchten, dass Ihre App unterstützt.

Das folgende Beispiel zeigt eine App-Manifestdatei für eine App, die alle Versionen von Windows von Windows Vista bis Windows 10:

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

Das Deklarieren der Windows 8.1 oder Windows 10 in Ihrem App-Manifest hat keine Auswirkungen, wenn Sie Ihre App unter vorherigen Betriebssystemen ausführen.

Das obige App-Manifest enthält auch den [ **&lt; &gt; TrustInfo-Abschnitt**](/previous-versions/bb756929(v=msdn.10)), der angibt, wie das System es in Bezug auf die Benutzerkontensteuerung [(User Account Control, UAC) behandeln soll.](/windows/security/identity-protection/user-account-control/how-user-account-control-works) Das **Hinzufügen von trustInfo** ist nicht unbedingt erforderlich, wird jedoch dringend empfohlen, auch wenn Ihre App kein bestimmtes UAC-bezogenes Verhalten benötigt. Insbesondere wenn Sie **"trustInfo"** überhaupt nicht hinzufügen, unterliegen 32-Bit-x86-Versionen Ihrer App der UAC-Dateivirtualisierung, die Schreibvorgänge in Ordner mit Administratorberechtigungen wie die Windows-Systemordner erfolgreich ausführen kann, wenn andernfalls ein Fehler auftrat, diese jedoch an einen benutzerspezifischen Ordner "VirtualStore" umgeleitet werden. [](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen der Systemversion](getting-the-system-version.md)
</dt> <dt>

[Versionshilfefunktionen](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
