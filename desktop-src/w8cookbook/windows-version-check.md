---
title: Windows-Versionsprüfung
description: Die Betriebssystemversion wurde mit dem Betriebssystemversions Windows 10 erhöht.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007880"
---
# <a name="windows-version-check"></a>Windows-Versionsprüfung

Die Betriebssystemversion wurde mit dem Betriebssystemversions Windows 10 erhöht. Dies bedeutet, dass die interne Versionsnummer für Windows 10 auch in 10.0 geändert wurde. Die Anwendungs- und Gerätekompatibilität nach einer Änderung der Betriebssystemversion aufrechtzuerhalten, war uns schon immer sehr wichtig. Bei den meisten App-Kategorien (ohne Kernelabhängigkeiten) wirkt sich die Änderung nicht negativ auf die App-Funktionalität aus, und vorhandene Apps funktionieren weiterhin einwandfrei Windows 10.

## <a name="manifestations"></a>Manifestationen

Inwieweit sich diese Änderung auswirkt, richtet sich nach der jeweiligen App. Dies bedeutet, dass alle Apps, die die Betriebssystemversion überprüfen, eine höhere Versionsnummer erhalten, was sich wie folgt äußern kann:

-   Apps können von App-Installern u. U. nicht installiert werden und nicht starten.
-   Apps können instabil werden oder abstürzen.
-   Apps können Fehlermeldungen ausgeben, aber weiterhin ordnungsgemäß funktionieren.

Einige Apps überprüfen die Version und geben einfach eine Warnung an den Benutzer aus. Es gibt jedoch auch Apps, für die eine Versionsprüfung unumgänglich ist (in den Treibern oder im Kernelmodus, um eine Erkennung zu vermeiden). In diesen Fällen verursacht die App beim Auffinden einer falschen Version einen Fehler. Wir empfehlen statt einer Versionsprüfung eines der folgenden Verfahren:

-   Wenn die App von bestimmten API-Funktionen abhängig ist, stellen Sie sicher, dass sie auf die richtige API-Version ausgerichtet ist.
-   Die Versionsnummer von NTDDI (NT-Gerätetreiberschnittstelle) wird nur erhöht, wenn sich die Zielfunktionalität in der API ändert. Stellen Sie sicher, dass Sie die Änderung über APISet oder eine andere verfügbar gemachte API erkennen, die vom Featureteam erstellt wurde, und die Version nicht als Proxy für ein Feature oder eine Korrektur verwenden. Wenn für bedeutende Änderungen keine ordnungsgemäße Prüfung verfügbar gemacht wird, liegt ein Fehler vor.
-   Stellen Sie sicher, dass die App NICHT auf ungerade Weise auf Version überprüft, z. B. über die Registrierung, Dateiversionen, Offsets, den Kernelmodus, Treiber oder andere Mittel. Wenn die App unbedingt die Version überprüfen muss, verwenden Sie die GetVersion-APIs, die die Haupt-, Neben- und Buildnummer zurückgeben sollten.
-   Wenn Sie die GetVersion-API oder andere Versionshilfefunktionen wie [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)verwenden, denken Sie daran, dass sich das Verhalten dieser API ab dem Windows 8.1. Weitere Informationen finden [Sie in der API-Dokumentation.](../SysInfo/version-helper-apis.md)
-   Wenn Sie Apps wie Antischadsoftware oder Firewall besitzen, sollten Sie ihre üblichen Feedbackkanäle und das Windows Insider-Programm verwenden.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>Deklarieren Windows 10 Kompatibilität mit einem App-Manifest

Wenn Ihre App mit Windows 10 kompatibel ist, kann sie diese Tatsache im [App-Manifest (ausführbares Manifest)](/windows/compatibility/application-executable-manifest) für die ausführbare Datei der App deklarieren. Dadurch wird dem System angezeigt, dass Ihre App die Systemversionsnummer 10.0 von Windows 10 versteht (sodass die GetVersion-API keine frühere Version zurück gibt) und das System auch andere Kompatibilitätsverhalten deaktivieren kann, die auf Apps angewendet werden, die keine Windows 10-Kompatibilität deklarieren.

Um Windows 10-Kompatibilität in einem App-Manifest zu deklarieren, [ **&lt; &gt;**](../SbsCs/application-manifests.md#compatibility) müssen Sie einen Kompatibilitätsabschnitt des Manifests hinzufügen, sofern noch nicht vorhanden, und dann **&lt; &gt; unterstützteOS-Elemente** für Windows 10 und jede andere Windows-Version hinzufügen, die Sie deklarieren möchten, dass Ihre App unterstützt.

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

Die oben markierte Zeile zeigt, wie Sie Ihre Anwendung genau auf `* ADD THIS LINE *` die Windows 10.

Das Deklarieren der Windows 10 in Ihrem App-Manifest hat keine Auswirkungen, wenn Sie Ihre App auf vorherigen Betriebssystemen ausführen.

## <a name="resources"></a>Ressourcen

-   [Download des Anwendungskompatibilitätstoolkits: Laden Sie das Windows ADK für Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Bekannte Kompatibilitätskorrekturen, Kompatibilitätsmodi und AppHelp-Meldungen](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [Versionshilfe-API](../sysinfo/version-helper-apis.md)