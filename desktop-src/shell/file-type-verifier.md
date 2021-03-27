---
description: Der Dateityp Verifier ist ein Tool, mit dem unabhängige Softwarehersteller überprüfen können, ob Ihre eindeutigen Dateitypen ordnungsgemäß implementiert werden.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Dateityp Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864948"
---
# <a name="file-type-verifier"></a>Dateityp Überprüfung

Der Dateityp Verifier ist ein Tool, mit dem unabhängige Softwarehersteller überprüfen können, ob Ihre eindeutigen Dateitypen ordnungsgemäß implementiert werden. Hochwertige Implementierungen ihrer Dateityp Handler sind für eine gute Benutzer Leistung von entscheidender Bedeutung, da Benutzer in Windows-Explorer auf vielerlei Weise mit Ihrem Dateiformat interagieren. Benutzer können voll Text suchen durchführen, nach benutzerdefinierten Metadaten sortieren oder umfassende Miniaturansichten und Vorschau Versionen Ihres Datei Formats anzeigen.

Anweisungen zur Verwendung der Dateityp Überprüfung finden Sie unter [Verwenden des Dateityp-verifizierers](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Informationen zum Dateityp-Verifier-Tool

Der Dateityp Verifier ist ein Programm, das als Teil des [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)verfügbar ist. Es wurde entwickelt, um Entwicklern zu helfen, die benutzerdefinierte Windows- [Dateitypen](fa-file-types.md) erstellen, um potenzielle Probleme mit ihren Dateitypen zu erkennen. Obwohl der Dateityp Verifier nur unter Windows 7 und höher ausgeführt wird, gelten die Regeln, die vom Dateityp Verifier erzwungen werden, für alle Windows-Versionen, auf denen die von ihm überprüfen Features verfügbar sind.

Die Dateityp Überprüfung führt verschiedene Tests für den Dateityp aus, um sicherzustellen, dass Sie ordnungsgemäß registriert ist, und stellt die entsprechenden [Dateityp Handler](fa-file-extensions.md) bereit, um den Dateityp in Windows-Explorer ordnungsgemäß anzuzeigen, und wenn dies der Fall ist, wird die Indizierung des Datei Inhalts unterstützt.

Der Dateityp Verifier testet Folgendes:

-   [Vorschau Handler](building-preview-handlers.md)
-   [Miniatur Ansichts Handler](building-thumbnail-providers.md)
-   [Eigenschaften Handler](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Verb Handler](fa-verbs.md)
-   [Filter (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Kind-Zuordnungen](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Wahrgenommene Typen](fa-perceivedtypes.md)
-   [Wichtige Eigenschaften](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Dateityp-verifizierers](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 
