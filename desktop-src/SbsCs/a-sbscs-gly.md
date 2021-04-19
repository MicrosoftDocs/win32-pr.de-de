---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (isolierte Anwendungen und parallele Assemblys)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347989"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (isolierte Anwendungen und parallele Assemblys)

a B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**Aktivierungs Kontext**
</dt> <dd>

Eine Datenstruktur im Arbeitsspeicher. Jeder Abschnitt dieser Struktur enthält Metadaten für parallele API-Funktionen. Ein Abschnitt kann z. b. dll-Umleitungs Daten enthalten, die vom dll-Lade Modul verwendet werden, und ein anderer Abschnitt kann über com-Serverdaten verfügen. Diese Daten können verwendet werden, um das Laden einer DLL an eine bestimmte Version, die Erstellung eines COM-Objekts oder die Erstellung eines Fensters an eine Version umzuleiten, die für die Anwendung am meisten kompatibel ist.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**Anwendungskonfiguration**
</dt> <dd>

Namen und Versionen paralleler Assemblys, die zum Ausführen einer Anwendung erforderlich sind. Wenn eine Anwendung mit einem Manifest bereitgestellt wird, werden Abhängigkeiten von bestimmten Versionen von freigegebenen parallelen Assemblys explizit definiert. Standardmäßig ist die Version der Assembly, die im Manifest angegeben ist, die Version, die bei der Aktivierung verwendet wird. Mit der globalen Anwendungskonfiguration wird die Konfiguration aller Anwendungen auf dem System festgelegt. Die Konfiguration pro Anwendung kann die globale Anwendungskonfiguration auf Anwendungs Basis außer Kraft setzen.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**Anwendungs Konfigurations Manifest**
</dt> <dd>

Eine Datei, die parallele Assemblys angibt, die von einer vollständig oder teilweise isolierten Anwendung verwendet werden sollen. Dateien des Anwendungs konfigurationsmanifests werden im selben Ordner wie die ausführbare Datei der Anwendung installiert.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**Anwendungs Manifest**
</dt> <dd>

Datei, in der eine isolierte Anwendung beschrieben wird. Sie gibt die für die Ausführung der Anwendung erforderlichen Informationen an, einschließlich Abhängigkeiten von privaten Assemblys, bestimmte Versionen von freigegebenen Assemblys und Metadaten für private Assemblys. Der Name einer Anwendungs Manifest-Datei ist der Name der ausführbaren Datei der Anwendung, gefolgt von der Erweiterung ". Manifest". Beispielsweise wäre die Manifest-Datei für MySampleApp.exe MySampleApp.exe. manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**Stadtverordneten**
</dt> <dd>

Grundlegende Einheit für das benennen, binden, Versionieren, bereitstellen oder Konfigurieren eines Blocks von Programmiercode. Diese Codeassemblys können in DLLs oder COM-Assemblys abgelegt werden. Anwendungen mit allgemeiner Funktionalität können freigegebene Blöcke von Programmiercode ausführen, die als Module oder Codeassemblys bezeichnet werden. Die Infrastruktur für die sichere Freigabe von Assemblys wird als parallele assemblyfreigabe bezeichnet.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**Assemblymanifest**
</dt> <dd>

Beschreibung einer parallelen Assembly. Er gibt den Namen, die Version, die Dateien, die Ressourcen der Assembly, die Bindungs Daten für die Elemente der Assembly sowie Abhängigkeiten von anderen parallelen Assemblys an. Eine Assemblymanifest-Datei kann einen beliebigen gültigen Dateinamen aufweisen, solange die Erweiterung. Manifest folgt.

</dd> </dl>

 

 



