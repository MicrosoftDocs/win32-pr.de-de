---
description: Neben assemblys werden mit den folgenden Typen von Manifest- und Konfigurationsdateien verwendet. Manifeste und Konfigurationen sind XML-Dateien.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referenz zu Manifestdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87636a8a4e5398cf9bb274d5ea8b9e7620104989322a20138a162ca45d9caf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142063"
---
# <a name="manifest-files-reference"></a>Referenz zu Manifestdateien

Neben assemblys werden mit den folgenden Typen von Manifest- und Konfigurationsdateien verwendet. Manifeste und Konfigurationen sind XML-Dateien.



| Manifest                                                               | Beschreibung                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Assemblymanifeste](assembly-manifests.md)                           | Beschreibt die Namen, Versionen, Ressourcen und Assemblyabhängigkeiten von nebenseitigen Assemblys.                                                                                                               |
| [Anwendungsmanifeste](application-manifests.md)                     | Beschreibt die Namen und Versionen freigegebener, nebeneinander verwendeter Assemblys, an die die Anwendung zur Laufzeit gebunden werden soll, und enthält möglicherweise auch Metadaten für private, von der Anwendung verwendete assemblyseitige Assemblys. |
| [Anwendungskonfigurationsdateien](application-configuration-files.md) | Leitet die Assemblyversionen von Assemblyabhängigkeiten mithilfe der [Anwendungskonfiguration um.](per-application-configuration.md)                                                                            |
| [Publisher Konfigurationsdateien](publisher-configuration-files.md)     | Leitet die Assemblyversionen von Assemblyabhängigkeiten pro Assembly mithilfe einer [Herausgeberkonfiguration um.](publisher-configuration.md)                                                              |



 

Eine Liste des Manifestdateischemas finden Sie unter [Manifestdateischema](manifest-file-schema.md).

Eine Liste des Schemas der Anwendungskonfigurationsdatei finden Sie unter [Schema der Anwendungskonfigurationsdatei.](application-configuration-file-schema.md)

Eine Liste des Schemas der Herausgeberkonfigurationsdatei finden Sie unter Publisher [Configuration File Schema](publisher-configuration-file-schema.md).

Andere Technologien erweitern das format, das von Windows Versions- und Konfigurationsmanifesten verwendet wird. Entwickler sollten informationen zum Manifestformat in der Spezifischen Dokumentation für die verwendete Technologie finden. Beispiel:

-   [ClickOnce](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [Übersicht: Common Language Runtime (CLR)](/dotnet/standard/clr)
-   [Benutzerkontensteuerung (User Account Control, UAC)](/previous-versions/bb756929(v=msdn.10))

 

 
