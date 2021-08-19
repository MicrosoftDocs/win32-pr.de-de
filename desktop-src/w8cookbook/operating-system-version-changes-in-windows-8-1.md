---
title: Änderungen der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2
description: Änderungen der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882690"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>Änderungen der Betriebssystemversion in Windows 8.1 und Windows Server 2012 R2

## <a name="platforms"></a>Plattformen

**Clients –** Windows 8.1

**Server –** Windows Server 2012 R2

## <a name="description"></a>BESCHREIBUNG

Wir haben einige wichtige Änderungen an der Funktionsweise der GetVersion(Ex)-APIs in Windows 8.1 vorgenommen, weil unerwünschtes Kundenverhalten auf die Verwendung der GetVersion(Ex)-APIs in der Vergangenheit zurückzuführen ist.

In früheren Versionen von Windows gab der Aufruf der GetVersion(Ex)-APIs die tatsächliche Version des Betriebssystems zurück, es sei denn, der Prozess wurde durch einen App-Kompatibilitätss shim gemindert, um ihm eine andere Version zu geben. Dies erfolgte auf der Grundlage einer Mäßigung und war relativ unvollständig in Bezug auf die Anzahl der Prozesse, die Microsoft in einem Release halbwegs shimen konnte. Viele Anwendungen durchlaufen die Risse, da sie aufgrund von schlecht entworfenen Versionsüberprüfungen nicht shimmed wurden.

Der erste Grund für eine Versionsprüfung besteht darin, den Benutzer zu warnen, dass die Anwendung unter einer neueren Version des Betriebssystems ausgeführt werden muss. Aufgrund schlechter Überprüfungen würden Apps jedoch häufig fälschlicherweise warnen, dass sie auf Windows XP oder höher ausgeführt werden mussten, was natürlich das neueste Betriebssystem ist. In den meisten Fällen würde das neueste Betriebssystem die Anwendung ohne Probleme ausführen, wenn dies nicht bei diesen Überprüfungen der Fall wäre.

## <a name="manifestation"></a>Manifestation

In Windows 8.1 sind die GetVersion(Ex)-APIs veraltet. Das bedeutet, dass sie zwar weiterhin diese API-Funktionen aufrufen können, aber wenn Ihre App nicht speziell auf Windows 8.1 ausgerichtet ist, geben die Funktionen die Windows 8 Version (6.2) zurück.

## <a name="solution"></a>Lösung

### <a name="adding-an-app-manifest"></a>Hinzufügen eines App-Manifests

Damit Ihre App Windows 8.1 als Ziel verwenden kann, müssen Sie ein [App-Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der App einschließen. Anschließend müssen Sie im [ **&lt; &gt; Kompatibilitätsabschnitt**](../SbsCs/application-manifests.md#compatibility) des Manifests ein **&lt; &gt; supportedOS-Element** für jede Windows Version hinzufügen, die Sie deklarieren möchten, dass Ihre App unterstützt.

Das folgende Beispiel zeigt eine App-Manifestdatei für eine App, die alle Versionen von Windows von Windows Vista bis Windows 8.1 unterstützt:

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

Die oben markierte Zeile `* ADD THIS LINE *` zeigt, wie Sie Ihre Anwendung genau auf Windows 8.1 ausrichten.

Das Deklarieren der Unterstützung für Windows 8.1 in Ihrem App-Manifest hat keine Auswirkungen, wenn Ihre App unter vorherigen Betriebssystemen ausgeführt wird.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Verwenden von VersionHelpers anstelle von GetVersion(Ex)

Windows 8.1 werden neue Ersatz-API-Funktionen für GetVersion(Ex) eingeführt, die als VersionHelpers bezeichnet werden. Sie sind äußerst einfach zu verwenden. Alles, was Sie tun müssen, ist `#include <VersionHelpers.h>` . Die in der Headerdatei VersionHelpers.h verfügbaren Inlinefunktionen ermöglichen es Ihrem Code, zu fragen, ob das Betriebssystem eine bestimmte Version von Windows oder höher ist.

**Beispiel** Wenn Ihre Anwendung beispielsweise Windows 8 oder höher erfordert, verwenden Sie den folgenden Test:

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Die verfügbaren Funktionen der VersionHelper-API sind:

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

Je nach der gestellten Frage wird TRUE oder FALSE zurückgegeben, und Sie müssen nur das betriebssystem der Mindestebene definieren, das Sie unterstützen.

## <a name="resources"></a>Ressourcen

-   [Herunterladen des Anwendungskompatibilitätstoolkits](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Bekannte Kompatibilitätskorrekturen, Kompatibilitätsmodi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [VersionHelpers-APIs](../sysinfo/version-helper-apis.md)