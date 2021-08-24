---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: (Isolierte Anwendungen und nebeneinander seitige Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac40ba2393bb2d043957e04b8d34ca93fede605bbcd11ad601667e97f79f057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142720"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>(Isolierte Anwendungen und nebeneinander seitige Assemblys)

A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**Aktivierungskontext**
</dt> <dd>

Eine Datenstruktur im Arbeitsspeicher. Jeder Abschnitt dieser Struktur enthält Metadaten für nebenseitige API-Funktionen. Beispielsweise kann ein Abschnitt DLL-Umleitungsdaten enthalten, die vom DLL-Lader verwendet werden, und ein anderer Abschnitt kann COM-Serverdaten enthalten. Diese Daten können verwendet werden, um das Laden einer DLL zu einer bestimmten Version, die Erstellung eines COM-Objekts oder die Erstellung eines Fensters auf eine Version umzuleiten, die für die Anwendung am kompatibelsten ist.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**Anwendungskonfiguration**
</dt> <dd>

Namen und Versionen von nebenseitigen Assemblys, die zum Ausführen einer Anwendung erforderlich sind. Wenn eine Anwendung mit einem Manifest bereitgestellt wird, werden Abhängigkeiten von bestimmten Versionen von freigegebenen, nebeneinander verfügbaren Assemblys explizit definiert. Standardmäßig ist die im Manifest angegebene Version der Assembly die Version, die bei der Aktivierung verwendet wird. Globale Anwendungskonfiguration gibt die Konfiguration aller Anwendungen auf dem System an. Die anwendungsspezifische Konfiguration kann die globale Anwendungskonfiguration anwendungsspezifische überschreiben.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**Anwendungskonfigurationsmanifest**
</dt> <dd>

Eine Datei, die nebenseitige Assemblys angibt, die von einer vollständigen oder teilweise isolierten Anwendung verwendet werden sollen. Anwendungskonfigurationsmanifestdateien werden im gleichen Ordner wie die ausführbare Datei der Anwendung installiert.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**Anwendungsmanifest**
</dt> <dd>

Datei, die eine isolierte Anwendung beschreibt. Sie gibt die Informationen an, die zum Ausführen der Anwendung erforderlich sind, einschließlich Abhängigkeiten von privaten Assemblys, bestimmten Versionen freigegebener Assemblys und Metadaten für private Assemblys. Der Name einer Anwendungsmanifestdatei ist der Name der ausführbaren Anwendungsdatei gefolgt von der Erweiterung .manifest. Beispielsweise wäre MySampleApp.exe Manifestdatei MySampleApp.exe manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**Versammlung**
</dt> <dd>

Grundlegende Einheit für das Benennen, Binden, Versionieren, Bereitstellen oder Konfigurieren eines Blocks von Programmiercode. Diese Codeassemblys können in DLLs oder COM-Assemblys platziert werden. Anwendungen mit gemeinsamer Funktionalität können freigegebene Codeblöcke ausführen, die als Module oder Codeassemblys bezeichnet werden. Die Infrastruktur für die sichere Freigabe von Assemblys wird als gemeinsame Assemblyfreigabe bezeichnet.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**Assemblymanifest**
</dt> <dd>

Beschreibung einer nebeneinander angezeigten Assembly. Sie gibt den Namen, die Version, die Dateien, die Ressourcen der Assembly, die Bindungsdaten für Elemente der Assembly und Abhängigkeiten von anderen nebenseitigen Assemblys an. Eine Assemblymanifestdatei kann einen beliebigen gültigen Dateinamen haben, solange darauf die Erweiterung .manifest folgt.

</dd> </dl>

 

 



