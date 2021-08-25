---
description: Weiterentwicklung der SUPPORTS-Unterstützung über Windows Versionen hinweg
ms.assetid: a3bda96e-6a54-41b3-88d3-9da88d7c0416
title: Weiterentwicklung der SUPPORTS-Unterstützung über Windows Versionen hinweg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e08ff181cf34daa95710d5bf57a294703a88ef
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467897"
---
# <a name="evolution-of-mui-support-across-windows-versions"></a>Weiterentwicklung der SUPPORTS-Unterstützung über Windows Versionen hinweg

-   [Vor Windows Vista](#before-windows-vista)
-   [Windows Vista und darüber hinaus](#windows-vista-and-beyond)
    -   [Ein sprachneutrales/NAP-Betriebssystem](#a-language-neutralmui-operating-system)
    -   [Bereitstellungsszenarios sind vollständig AUF DEM BEREITSTELLUNGS-Basierten basieren.](#deployment-scenarios-are-fully-mui-based)
    -   [Bereitstellung eines einzelnen Images](#single-image-deployment)
    -   [Verbessertes Wartungsmodell](#improved-servicing-model)
    -   [INFRASTRUCTURE-Infrastruktur](#mui-infrastructure)
    -   [Sprachverwaltung](#language-management)
    -   [Ressourcenbehandlung](#resource-handling)

## <a name="before-windows-vista"></a>Vor Windows Vista

Vor der Version Windows Vista Windows mit Einzelsprachimages ausgeliefert, was bedeutete, dass jede lokalisierte Version von Windows eine einzelne Sprache für die Benutzeroberfläche enthielt. DIEs war ein Add-On zur englischen Version des Betriebssystems, und die mehrsprachige Benutzeroberfläche Packs konnten nur bestimmten englischen Versionen von Windows hinzugefügt werden. Bei der Installation auf der englischen Version von Windows erlaubte DIE LANGUAGE-Einstellung, dass die Sprache der Benutzeroberfläche des Betriebssystems gemäß den Einstellungen einzelner Benutzer in eine der unterstützten Sprachen geändert werden konnte.

Das MUI Pack-Modell hat keine SUPPORTS-Unterstützung für Anwendungen verfügbar gemacht. Obwohl Entwickler mehrsprachige Anwendungen erstellen konnten, mussten sie dafür eigene Mechanismen erstellen.

## <a name="windows-vista-and-beyond"></a>Windows Vista und darüber hinaus

Mit Windows Vista hat Microsoft eine erhebliche Investition in DAS UNTERNEHMEN getätigt. Windows Vista wird von Grund auf auf einer VISTA-Plattform erstellt. Dies ist zwar ein wichtiger Fortschritt in Windows Lokalisierungsstrategie, da es für Microsoft eine wichtige Möglichkeit ist, Windows in mehr Sprachen als je zuvor bereitzustellen, aber es ist für Windows Benutzer und Kunden ein großer Fortschritt.

### <a name="a-language-neutralmui-operating-system"></a>Ein sprachneutrales/NAP-Betriebssystem

Der Großteil der Windows Vista-Binärdateien ist MIT DEM-Standard konform, und ihre lokalisierbaren Daten werden getrennt vom Code gespeichert. Dies bietet Flexibilität, da jederzeit unterschiedliche Sprachdaten hinzugefügt werden können.

### <a name="deployment-scenarios-are-fully-mui-based"></a>Bereitstellungsszenarios sind vollständig AUF DER BASIS VON BEREITSTELLUNGEN basieren.

Die Windows Vista-Paketierungs- und -Installationsentwurf sind AUF DER BASIS VON, und alle lokalisierbaren Daten werden in sprachspezifischen Paketen gepackt, und jedes Sprachpaket kann in unterschiedlichen Szenarien bereitgestellt werden. Obwohl die Verkaufs-DVDs für Windows Vista z. B. Einzelsprachversionen enthalten, können Benutzer der Ultimate-Edition zusätzliche EDITIONS-Sprachpakete herunterladen und die Benutzeroberflächensprache über die Systemsteuerung **"Regionale Optionen" und "Sprachoptionen"** wechseln. Enterprise-Editionslizenzen erhalten alle Sprachen und können jede dieser Sprachen bereitstellen.

### <a name="single-image-deployment"></a>Bereitstellung eines einzelnen Images

Enterprise Kunden und OEMs können jetzt die Anzahl der Images reduzieren, die sie verwalten müssen, um Windows und Anwendungen auf Computern über verschiedene Gebietsschemas hinweg über die Bereitstellung einzelner Images bereitzustellen.

Mit DEM FOKUS auf Windows Vista kann ein Image mit mehreren Sprachen für alle Sprachbenutzer bereitgestellt werden, und Benutzer können ihre eigenen bevorzugten Sprachen (innerhalb der Richtlinie) während des Setups oder der anfänglichen "out-of-the-box"-Benutzeroberfläche mit dem Computer bestimmen. OeMs können insbesondere viele Benutzeroberflächensprachen auf ihren neuen Computern installieren, damit Benutzer eine der Begrüßungscenter auswählen können. Aus einem Bild mit mehreren Sprachpaketen zeigt Setup daher eine Liste der verfügbaren Sprachen an und ermöglicht Benutzern die Auswahl einer dieser Sprachen. Alle internationalen Einstellungen werden dann so festgelegt, dass sie mit der ausgewählten Sprache oder dem ausgewählten Gebietsschema übereinstimmen.

### <a name="improved-servicing-model"></a>Verbessertes Wartungsmodell

Das gleiche QFE- oder Sicherheitsfixpaket kann jetzt auf allen Sprachsystemen installiert werden. Dies ist wichtig, da sie insbesondere eine schnellere Verarbeitung von Sicherheitsfixes ermöglicht und es allen internationalen Benutzern ermöglicht, von der gleichen Zeitverfügbarkeit aller Sicherheitsfixes zu profitieren.

### <a name="mui-infrastructure"></a>INFRASTRUCTURE-Infrastruktur

Ab Windows Vista sind DIE APIs von CAB verfügbar, damit Entwickler die VORTEILE DER MECHANISMEN für ihre eigenen Anwendungen nutzen können, ohne benutzerdefinierte Logik für die Ressourcenbehandlung und Sprachverwaltung erstellen zu müssen.

### <a name="language-management"></a>Sprachverwaltung

BaseBASE-APIs, die Funktionen zur Verwaltung von Benutzeroberflächensprachen bereitstellen, sind als Teil der INFRASTRUCTURE-Infrastruktur verfügbar. Um die verschiedenen Einstellungen für die Benutzeroberflächensprache auf System-, Benutzer- und Anwendungsebene zu verwalten, werden diese intern in einer einzigen priorisierten Liste zusammengefasst. DANN implementiert DAS PROGRAMM einen Fallbackmechanismus, der auf dieser priorisierten Liste basiert, sodass Teillokalisierungslösungen möglich sind, während Benutzern eine geeignete , falls nicht bevorzugte Benutzeroberfläche zur Verfügung steht.

Beispielsweise kann ein System, auf dem die spanischen Version von Windows Vista mit einem Language Interface Pack (LIP) installiert ist, das auf dem Basisbetriebssystem installiert ist, folgendes Verhalten unterstützen: Das System versucht zunächst, seine Ressourcen in "Zuerst" anzuzeigen, und wenn diese Ressourcen nicht in "English" verfügbar sind, stellen Sie dem Benutzer stattdessen spanischen Ressourcen zur Verfügung.

### <a name="resource-handling"></a>Ressourcenbehandlung

Mit der verbesserten INFRASTRUCTURE-Infrastruktur, die ab Windows Vista verfügbar ist, sind die gängigsten Ressourcentechnologien FÜR DIE BEREITSTELLUNG aktiviert. Die folgende Tabelle enthält zusätzliche Details zur Unterstützung der Ressourcenbehandlung, die in Windows Vista verfügbar ist.




| Category | Support | 
|----------|---------|
| Unterstützte Ressourcentypen | <ul><li>Win32/nicht verwaltete Ressource: .DLL/.EXE/. OCX</li><li>Shell-bezogene Registrierungen</li><li>Verwaltungsbezogene Ressourcen: Ereignisprotokoll, Snap-In-/MSC-Dateien</li><li>WMI: MOF/MFL</li><li>Gruppenrichtlinie: ADMX/ADML</li><li>Verwaltete Resources.dll</li></ul> | 
| Entwicklungstools | <ul><li>Für Win32: RC.exe, MUIRCT.exe und Visual Studio 2005 und höher</li></ul> | 
| Eingeschränkte Ressourcentypunterstützung | <ul><li>*.chm-Hilfedateien</li></ul> | 




 

 

 



