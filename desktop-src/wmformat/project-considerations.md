---
title: Überlegungen zu Projekten
description: Überlegungen zu Projekten
ms.assetid: aebe2886-0af0-443a-a5be-651f11936639
keywords:
- Windows Media-Format-SDK, Projekt Überlegungen
- Advanced Systems Format (ASF), Projekt Überlegungen
- ASF (Advanced Systems Format), Projekt Überlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1682e8008569c9b230b2c2f53f394326669d022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207313"
---
# <a name="project-considerations"></a>Überlegungen zu Projekten

Sie müssen sicherstellen, dass der Endbenutzer Anwendungen, die Sie mit dem Windows Media Format SDK erstellen, ordnungsgemäß ausführen kann. In diesem Abschnitt werden zwei Aspekte beschrieben, die Sie beim Verteilen von Anwendungen, Dateinamen Erweiterungen und Software Weiterungen beachten müssen.

Sie müssen die richtigen Dateinamen Erweiterungen für alle Dateien verwenden, die mit Ihren Anwendungen erstellt wurden. Durch die Verwendung der richtigen Dateinamen Erweiterungen wird Endbenutzern das Erkennen von ASF-Dateien erleichtert, und es werden Verwirrung beim Decodieren von Dateien verhindert.

Sie müssen alle verteilbaren Komponenten bereitstellen, die zum Ausführen der Anwendungen erforderlich sind. Ohne die korrekten verteilbaren Komponenten können Benutzer ihre Anwendungen nicht verwenden.

In den folgenden Abschnitten werden Dateinamen Erweiterungen und die Software Verteilung ausführlich beschrieben.



| `Section`                                                                      | BESCHREIBUNG                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Richtlinien für die Dateinamenerweiterung](file-name-extension-guidelines.md)         | Enthält Informationen über die Dateinamen Erweiterungen, die Sie für die von Ihrem Programm erstellten ASF-Dateien verwenden sollten.     |
| [Software Verteilung](software-redistribution.md)                       | Beschreibt die verteilbaren Dateien für das Windows Media-Format-SDK und wie diese in Ihre Anwendungen aufgenommen werden. |
| [Anwendungs Abhängigkeit wird registriert](registering-application-dependency.md) | Beschreibt, wie Sie die Anwendung als abhängig von der SDK-Laufzeit des Windows Media-Formats registrieren.          |



 

 

 




