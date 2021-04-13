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
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Änderungen an der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2

## <a name="platforms"></a>Plattformen

**Clients:** Windows 8.1

**Server:** Windows Server 2012 R2

## <a name="description"></a>BESCHREIBUNG

Wir haben einige bedeutende Änderungen an der Funktionsweise der GetVersion (ex)-APIs in Windows 8.1 durchgeführt, weil unerwünschte Kunden Verhaltensweisen, die sich aus der Verwendung der GetVersion (ex)-APIs in der Vergangenheit ergeben haben.

In früheren Versionen von Windows gab das Aufrufen der GetVersion (ex)-APIs die tatsächliche Version des Betriebssystems (OS) zurück, es sei denn, der Prozess wurde durch eine APP Kompatibilitäts Shim verringert, um eine andere Version zu erhalten. Dies wurde vorläufig durchgeführt und war relativ unvollständig in Bezug auf die Anzahl der Prozesse, die Microsoft in einem Release in gewisser Weise verarbeitbaren. Viele Anwendungen haben die Risse durchlaufen, da Sie aufgrund von unzureichend entworfenen Versions Überprüfungen nicht geshimmt wurden.

Der einzige Grund, eine Versions Überprüfung durchzuführen, besteht darin, den Benutzer zu warnen, dass die Anwendung auf einer neueren Version des Betriebssystems ausgeführt werden muss. Aufgrund von schlechten Überprüfungen würden apps jedoch häufig fälschlicherweise gewarnt, dass Sie unter Windows XP oder höher ausgeführt werden müssen, was natürlich das neueste Betriebssystem ist. Meistens führt das neueste Betriebssystem die Anwendung ohne Probleme aus, wenn dies nicht für diese Überprüfungen der Fall ist.

## <a name="manifestation"></a>Ausstrahlung

In Windows 8.1 wurden die GetVersion (ex)-APIs als veraltet markiert. Dies bedeutet, dass Sie die Windows 8-Version (6,2) zurückgeben können, während Sie diese API-Funktionen weiterhin abrufen können, wenn Ihre APP nicht speziell auf Windows 8.1 ausgerichtet ist.

## <a name="solution"></a>Lösung

### <a name="adding-an-app-manifest"></a>Hinzufügen eines App-Manifests

Damit Ihre APP auf Windows 8.1 abzielen kann, müssen Sie ein [App-Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP einschließen. Anschließend müssen Sie im [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests ein **&lt; SupportedOS &gt;** -Element für jede Windows-Version hinzufügen, die von ihrer App unterstützt wird.

Das folgende Beispiel zeigt eine APP-Manifest-Datei für eine APP, die alle Versionen von Windows von Windows Vista bis Windows 8.1 unterstützt:

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

Die oben markierte Zeile `* ADD THIS LINE *` zeigt, wie Sie Ihre Anwendung für Windows 8.1 genau ausrichten können.

Das Deklarieren der Unterstützung für Windows 8.1 im App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Verwenden von versionhilfsprogramme anstelle von GetVersion (ex)

Windows 8.1 führt neue Ersetzungs-API-Funktionen für GetVersion (ex) ein, die als versionhilfsprogramme bezeichnet werden. Sie sind äußerst einfach zu verwenden. alles, was Sie tun müssen `#include <VersionHelpers.h>` . Mit den Inline Funktionen, die in der Header Datei "versionhilfsprogramme. h" verfügbar sind, kann Ihr Code Fragen, ob das Betriebssystem eine bestimmte Version von Windows oder höher ist.

**Beispiel** Wenn Ihre Anwendung z. b. Windows 8 oder höher erfordert, verwenden Sie den folgenden Test:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Die folgenden versionhelper-API-Funktionen sind verfügbar:

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

Abhängig von der Frage, die Sie anfordern, wird "true" oder "false" zurückgegeben, und Sie müssen nur das Betriebssystem auf Mindestebene definieren, das Sie unterstützen.

## <a name="resources"></a>Ressourcen

-   [Anwendungskompatibilitäts-Toolkit Download](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Versionhilfsprogramme-APIs](../sysinfo/version-helper-apis.md)