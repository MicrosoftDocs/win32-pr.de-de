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
# <a name="windows-version-check"></a>Windows-Versionsprüfung

Die Betriebssystemversion wurde mit dem Windows 10-Betriebssystem Release inkrementiert. Dies bedeutet, dass die interne Versionsnummer für Windows 10 auch in 10,0 geändert wurde. Die Anwendungs- und Gerätekompatibilität nach einer Änderung der Betriebssystemversion aufrechtzuerhalten, war uns schon immer sehr wichtig. Bei den meisten App-Kategorien (ohne Kernel Abhängigkeiten) wirkt sich die Änderung nicht negativ auf die APP-Funktionalität aus, und vorhandene apps funktionieren unter Windows 10 weiterhin einwandfrei.

## <a name="manifestations"></a>Kundgebungen

Inwieweit sich diese Änderung auswirkt, richtet sich nach der jeweiligen App. Dies bedeutet, dass alle Apps, die die Betriebssystemversion überprüfen, eine höhere Versionsnummer erhalten, was sich wie folgt äußern kann:

-   Apps können von App-Installern u. U. nicht installiert werden und nicht starten.
-   Apps können instabil werden oder abstürzen.
-   Apps können Fehlermeldungen ausgeben, aber weiterhin ordnungsgemäß funktionieren.

Einige Apps überprüfen die Version und geben einfach eine Warnung an den Benutzer aus. Es gibt jedoch auch Apps, für die eine Versionsprüfung unumgänglich ist (in den Treibern oder im Kernelmodus, um eine Erkennung zu vermeiden). In diesen Fällen verursacht die App beim Auffinden einer falschen Version einen Fehler. Wir empfehlen statt einer Versionsprüfung eines der folgenden Verfahren:

-   Wenn die App von bestimmten API-Funktionen abhängig ist, stellen Sie sicher, dass sie auf die richtige API-Version ausgerichtet ist.
-   Die Versionsnummer von ntddi (NT-Gerätetreiber Schnittstelle) wird nur erhöht, wenn sich die Ziel Funktionalität in der API ändert. Stellen Sie sicher, dass Sie die Änderung mithilfe von apiset oder einer anderen verfügbar gemachten API erkennen, wie Sie vom Featureteam erstellt wurde, und verwenden Sie die Version nicht als Proxy für ein Feature oder eine Korrektur. Wenn für bedeutende Änderungen keine ordnungsgemäße Prüfung verfügbar gemacht wird, liegt ein Fehler vor.
-   Stellen Sie sicher, dass die APP nicht auf ungerade Weise auf eine Version prüft, wie z. b. über die Registrierung, Dateiversionen, Offsets, Kernel Modus, Treiber oder andere Mittel. Wenn die APP unbedingt die Version überprüfen muss, verwenden Sie die GetVersion-APIs, die die Haupt-, neben-und Buildnummer zurückgeben.
-   Wenn Sie die GetVersion-API oder andere Versions Hilfsobjekte wie [verifyversioninfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)verwenden, denken Sie daran, dass sich das Verhalten dieser API beginnend mit Windows 8.1 geändert hat. Weitere Informationen finden Sie in [der API-Dokumentation](../SysInfo/version-helper-apis.md) .
-   Wenn Sie apps wie Antischadsoftware oder Firewall besitzen, sollten Sie über ihre üblichen Feedback Kanäle und über das Windows Insider-Programm arbeiten.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>Deklarieren der Windows 10-Kompatibilität mit einem App-Manifest

Wenn Ihre APP mit Windows 10 kompatibel ist, kann Sie diese Tatsache im APP- [Manifest (ausführbare Datei)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der APP deklarieren. Dadurch wird dem System mitgeteilt, dass Ihre APP die System Versionsnummer 10,0 von Windows 10 versteht (sodass die GetVersion-API keine frühere Version zurückgibt). Außerdem kann das System andere Kompatibilitäts Verhalten deaktivieren, die auf apps angewendet werden, die keine Windows 10-Kompatibilität deklarieren.

Um die Windows 10-Kompatibilität in einem App-Manifest zu deklarieren, müssen Sie einen [ **&lt; Kompatibilitäts &gt;** Abschnitt](../SbsCs/application-manifests.md#compatibility) des Manifests hinzufügen, sofern noch nicht vorhanden. Fügen Sie dann **&lt; SupportedOS &gt;** -Elemente für Windows 10 und jede andere Windows-Version hinzu, die von ihrer App unterstützt wird.

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

Die oben markierte Zeile `* ADD THIS LINE *` zeigt, wie Sie Ihre Anwendung für Windows 10 genau ausrichten können.

Das Deklarieren der Unterstützung für Windows 10 in Ihrem App-Manifest hat keine Auswirkung, wenn Sie Ihre APP unter früheren Betriebssystemen ausführen.

## <a name="resources"></a>Ressourcen

-   [Download des Anwendungskompatibilitäts-Toolkits: Herunterladen des Windows ADK für Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Bekannte Kompatibilitäts Korrekturen, Kompatibilitäts Modi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API für Versions Hilfsprogramme](../sysinfo/version-helper-apis.md)