---
description: Entwicklung der MUI-Unterstützung in Windows-Versionen
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Entwicklung der MUI-Unterstützung in Windows-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b896c3651cbea3eef8f2d2021194742f24818f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362548"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Entwicklung der MUI-Unterstützung in Windows-Versionen

-   [Vor Windows Vista](#before-windows-vista)
-   [Windows Vista und darüber hinaus](#windows-vista-and-beyond)
    -   [Ein sprach neutrales/MUI-Betriebssystem](#a-language-neutralmui-operating-system)
    -   [Bereitstellungs Szenarien sind vollständig MUI-basiert](#deployment-scenarios-are-fully-mui-based)
    -   [Bereitstellung mit einem Image](#single-image-deployment)
    -   [Verbessertes Wartungs Modell](#improved-servicing-model)
    -   [MUI-Infrastruktur](#mui-infrastructure)
    -   [Sprach Verwaltung](#language-management)
    -   [Ressourcen Behandlung](#resource-handling)

## <a name="before-windows-vista"></a>Vor Windows Vista

Vor der Windows Vista-Version waren Windows mit einsprachigen Images ausgeliefert, was bedeutete, dass jede lokalisierte Version von Windows eine einzige Sprache für Ihre Benutzeroberfläche enthielt. MUI war ein Add-on für die englische Version des Betriebssystems, und die mehrsprachigen Benutzeroberflächen Pakete konnten nur bestimmten englischen Windows-Versionen hinzugefügt werden. Bei der Installation unter der englischen Version von Windows erlaubte MUI die Benutzeroberflächen Sprache des Betriebssystems entsprechend den Einstellungen einzelner Benutzer für eine der unterstützten Sprachen zu ändern.

Das MUI Pack Modell hat die MUI-Unterstützung für Anwendungen nicht verfügbar gemacht. Obwohl Entwickler mehrsprachige Anwendungen erstellen konnten, mussten Sie dafür eigene Mechanismen erstellen.

## <a name="windows-vista-and-beyond"></a>Windows Vista und darüber hinaus

Mit Windows Vista machte Microsoft bedeutende Investitionen in MUI. Windows Vista wurde von Grund auf auf einer MUI-Plattform erstellt. Obwohl dies ein wichtiger Fortschritt in der Windows-Lokalisierungsstrategie darstellt, ist es ein wichtiger Faktor für Microsoft, Windows in mehr Sprachen als je zuvor bereitzustellen. es ist vor allem eine gute Voraussetzung für Windows-Benutzer und-Kunden.

### <a name="a-language-neutralmui-operating-system"></a>Ein sprach neutrales/MUI-Betriebssystem

Die meisten Windows Vista-Binärdateien sind MUI-konform, und ihre lokalisierbaren Daten werden getrennt vom Code gespeichert. Dies bietet Flexibilität, da jeweils unterschiedliche Sprach Daten hinzugefügt werden können.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Bereitstellungs Szenarien sind vollständig MUI-basiert

Der Verpackungs-und Installations Entwurf von Windows Vista ist MUI-basiert, und alle lokalisierbaren Daten werden in sprachspezifischen Paketen verpackt, und die einzelnen Sprachpakete können in verschiedenen Szenarien bereitgestellt werden. Obwohl die Einzelhandels-DVDs für Windows Vista einzelne Sprachversionen enthalten, können Benutzer der Ultimate-Edition zusätzliche MUI Language Packs herunterladen und die Benutzeroberflächen Sprache über die Systemsteuerung für Regions **-und Sprachoptionen** wechseln. Lizenznehmer von Enterprise Edition erhalten alle Sprachen und können diese bereitstellen.

### <a name="single-image-deployment"></a>Bereitstellung mit einem Image

Unternehmenskunden und-OEMs können nun die Anzahl der abzurufenden Images reduzieren, um Windows und Anwendungen auf Computern über verschiedene Gebiets Schemas über eine Bereitstellung mit nur einem Image bereitzustellen.

Mit MUI unter Windows Vista kann ein Bild, das mehrere Sprachen enthält, für beliebige Benutzer bereitgestellt werden, und Benutzer können Ihre eigenen bevorzugten Sprachen (innerhalb der Richtlinie) während des Setups oder die anfängliche "Standarddarstellung" mit dem Computer ermitteln. Insbesondere können OEMs viele Benutzeroberflächen Sprachen auf Ihren neuen Computern ablegen, um Benutzern die Auswahl aus dem Begrüßungs Center zu ermöglichen. Daher wird von einem Bild mit mehreren Sprachpaketen eine Liste der verfügbaren Sprachen angezeigt, und Benutzer können eine der verfügbaren Sprachen auswählen. Alle internationalen Einstellungen werden dann entsprechend der ausgewählten Sprache oder dem ausgewählten Gebiets Schema festgelegt.

### <a name="improved-servicing-model"></a>Verbessertes Wartungs Modell

Das gleiche QFE-oder sicherheitsfixpaket kann nun auf allen Sprachsystemen installiert werden. Dies ist wichtig, da es einen schnelleren Trend der Sicherheitskorrekturen ermöglicht und es allen internationalen Benutzern ermöglicht wird, von der gleichen Zeit für alle Sicherheitskorrekturen zu profitieren.

### <a name="mui-infrastructure"></a>MUI-Infrastruktur

Ab Windows Vista sind MUI-APIs verfügbar, mit denen Entwickler die MUI-Mechanismen für Ihre eigenen Anwendungen nutzen können, ohne benutzerdefinierte Logik für die Ressourcenverarbeitung und sprach Verwaltung erstellen zu müssen.

### <a name="language-management"></a>Sprach Verwaltung

Grundlegende MUI-APIs, die Verwaltungsfunktionen für die Benutzeroberfläche bereitstellen, sind als Teil der MUI-Infrastruktur verfügbar. Um die verschiedenen Einstellungen der Benutzeroberflächen Sprache auf System-, Benutzer-und Anwendungsebene verwalten zu können, kombiniert MUI Sie intern zu einer einzigen priorisierten Liste. MUI implementiert dann auf der Grundlage dieser priorisierten Liste einen Fall Back Mechanismus, der partielle Lokalisierungslösungen ermöglicht und Benutzern eine angemessene –, falls nicht gewünscht – Benutzeroberflächen Sprache bereitstellt.

Beispielsweise kann ein System, auf dem die spanische Version von Windows Vista mit einem auf dem Basis Betriebssystem installierten Sprachschnittstellen Paket (Sync Language Interface Pack) ausgeführt wird, das folgende Verhalten unterstützen: das System versucht, seine Ressourcen zuerst in Katalanisch anzuzeigen. wenn diese Ressourcen nicht in Katalanisch verfügbar sind, sollten Sie dem Benutzer stattdessen spanische Ressourcen bereitstellen.

### <a name="resource-handling"></a>Ressourcen Behandlung

Mit der verbesserten MUI-Infrastruktur, die ab Windows Vista verfügbar ist, sind die meisten gängigen Ressourcen Technologien MUI-fähig. In der folgenden Tabelle finden Sie weitere Informationen zur Unterstützung der Ressourcen Behandlung in Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Category</th>
<th>Support</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unterstützte Ressourcentypen</td>
<td><ul>
<li>Win32/nicht verwaltete Ressource:. DLL/. EXE/. OCX</li>
<li>Shell-bezogene Registrierungen</li>
<li>Verwaltungs bezogene Ressourcen: Ereignisprotokoll, Snap-in/MSC-Dateien</li>
<li>WMI: MOF/MFL</li>
<li>Gruppenrichtlinie: ADMX/ADML</li>
<li>Verwaltete Resources.dll</li>
</ul></td>
</tr>
<tr class="even">
<td>Entwicklungstools</td>
<td><ul>
<li>Für Win32: RC.exe, MUIRCT.exe und Visual Studio 2005 und höher</li>
</ul></td>
</tr>
<tr class="odd">
<td>Eingeschränkte Ressourcentyp Unterstützung</td>
<td><ul>
<li>*. chm-Hilfedateien</li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



