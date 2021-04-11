---
description: Parallele Assemblys werden mit den folgenden Typen von Manifest-und Konfigurationsdateien verwendet. Manifeste und Konfigurationen sind XML-Dateien.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Manifest-Dateireferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128820"
---
# <a name="manifest-files-reference"></a>Manifest-Dateireferenz

Parallele Assemblys werden mit den folgenden Typen von Manifest-und Konfigurationsdateien verwendet. Manifeste und Konfigurationen sind XML-Dateien.



| Manifest                                                               | BESCHREIBUNG                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Assembly-Manifeste](assembly-manifests.md)                           | Beschreibt die Namen, Versionen, Ressourcen und Assemblyabhängigkeiten von parallelen Assemblys.                                                                                                               |
| [Anwendungs Manifeste](application-manifests.md)                     | Beschreibt die Namen und Versionen von freigegebenen parallelen Assemblys, die von der Anwendung zur Laufzeit gebunden werden sollen und die auch Metadaten für private parallele Assemblys enthalten, die von der Anwendung verwendet werden. |
| [Anwendungs Konfigurationsdateien](application-configuration-files.md) | Leitet die Assemblyversionen von Assemblyabhängigkeiten mithilfe einer [Konfiguration pro Anwendung](per-application-configuration.md)um.                                                                            |
| [Verleger Konfigurationsdateien](publisher-configuration-files.md)     | Leitet die Assemblyversionen von Assemblyabhängigkeiten pro Assembly mithilfe einer [Herausgeber Konfiguration](publisher-configuration.md)um.                                                              |



 

Eine Auflistung des Manifest-Datei Schemas finden Sie unter [Manifest-Datei Schema](manifest-file-schema.md).

Eine Auflistung des Schemas der Anwendungs Konfigurationsdatei finden Sie unter [Schema der Anwendungs Konfigurationsdatei](application-configuration-file-schema.md).

Eine Auflistung des Schema der Verleger Konfigurationsdatei finden Sie unter [Schema der Verleger Konfigurationsdatei](publisher-configuration-file-schema.md).

Andere Technologien erweitern das von der Windows-Versionsverwaltung und Konfigurations Manifeste verwendete Format. Entwickler sollten sich auf die Dokumentation beziehen, die sich speziell auf die Technologie bezieht, die für Informationen über das Manifest-Format verwendet wird. Beispiel:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Übersicht: Common Language Runtime (CLR)](/dotnet/standard/clr)
-   [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/bb756929(v=msdn.10))

 

 
