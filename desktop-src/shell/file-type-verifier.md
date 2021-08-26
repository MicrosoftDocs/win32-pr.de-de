---
description: Die Dateityp-Überprüfung ist ein Tool, mit dem unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) überprüfen können, ob ihre eindeutigen Dateitypen ordnungsgemäß implementiert sind.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Dateitypverifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad3d3e66d85413a209c6899ce16061fa1fd46468fa32462026485d49b7326dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009510"
---
# <a name="file-type-verifier"></a>Dateitypverifizierer

Die Dateityp-Überprüfung ist ein Tool, mit dem unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) überprüfen können, ob ihre eindeutigen Dateitypen ordnungsgemäß implementiert sind. Qualitativ hochwertige Implementierungen Ihrer Dateityphandler sind entscheidend für eine gute Benutzererfahrung, da Benutzer im Explorer auf viele Arten mit Ihrem Dateiformat Windows interagieren. Benutzer können Volltextsuchen durchführen, nach benutzerdefinierten Metadaten sortieren oder umfangreiche Miniaturansichten und Vorschauen Ihres Dateiformats anzeigen.

Anweisungen zur Verwendung der Dateitypverifizierer finden Sie unter [How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Informationen zum Tool zum Verifizieren von Dateitypen

File Type Verifier ist ein Programm, das als Teil des sdk Windows [7 verfügbar ist.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Es soll Entwicklern helfen, benutzerdefinierte [Windows-Dateitypen zu](fa-file-types.md) erstellen, um potenzielle Probleme mit ihren Dateitypen zu erkennen. Obwohl die Dateitypüberprüfung nur unter Windows 7 und höher ausgeführt wird, gelten die Regeln, die von der Dateitypüberprüfung erzwungen werden, für alle Versionen von Windows, in denen die überprüften Funktionen verfügbar sind.

Der Dateitypverifizierer führt mehrere Tests für den Dateityp aus, um zu überprüfen, ob er ordnungsgemäß registriert ist, und stellt die entsprechenden Dateityphandler zum ordnungsgemäßen Anzeigen des [Dateityps](fa-file-extensions.md) im Windows-Explorer und gegebenenfalls zur Unterstützung der Indizierung des Dateiinhalts zur Auswahl.

Die Dateitypprüfung testet Folgendes:

-   [Vorschauhandler](building-preview-handlers.md)
-   [Miniaturansichtshandler](building-thumbnail-providers.md)
-   [Eigenschaftenhandler](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Verbhandler](fa-verbs.md)
-   [Filter (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Artzuordnungen](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Wahrgenommene Typen](fa-perceivedtypes.md)
-   [Wichtige Eigenschaften](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Dateitypverifizierer](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Funktionsweise von Dateizuordnungen](fa-how-work.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 
