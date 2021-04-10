---
description: Das Search-MS?-Anwendungsprotokoll ist eine Konvention zum Abfragen des Windows-Suchindex.
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: Die ersten Schritte mit Parameter-Value Argumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214455"
---
# <a name="getting-started-with-parameter-value-arguments"></a>Die ersten Schritte mit Parameter-Value Argumenten

Die **Such-MS** ? Das [Anwendungsprotokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine Konvention zum Abfragen des Windows-Suchindex. Das Protokoll ermöglicht Anwendungen wie Windows-Explorer, den Index mit Parameter-Wert-Argumenten abzufragen, einschließlich Eigenschafts Argumenten, zuvor gespeicherter Suchvorgänge, erweiterter Abfrage Syntax (AQS), natürlicher Abfrage Syntax (NQS) und Sprachcode Bezeichner (LCIDs) für den Indexer und die Abfrage selbst.

Dieses Thema ist wie folgt organisiert:

- [Informationen zu Parameter-Value Argumenten](#about-parameter-value-arguments)
- [Beispiele](#examples)
- [Zugehörige Themen](#related-topics)

## <a name="about-parameter-value-arguments"></a>Informationen zu Parameter-Value Argumenten

Das Search-MS-Protokoll verwendet die folgende standardmäßige URL-codierte Syntax:

```
search-ms:parameter=value[&parameter=value]&
```

Die Syntax beginnt mit der Identifizierung des Protokolls selbst (Search-MS:). Die Parameter/Wert-Paare sind Argumente, die an die Such-Engine übergeben werden, wie in der folgenden Tabelle beschrieben.

| Parameter                                                    | Wert                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                | Version                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| Abfrage                                                        | URL-codierter Text                                              | Der vom Benutzer eingegebene Abfragetext.                                                                                                                                                                                                                                        | Windows XP und höher    |
| [InputLocale](-search-3x-wds-qryidx-localeidentifiers.md)   | Eine beliebige gültige LCID                                                | Die LCID, die die Eingabe Sprache für die Abfrage identifiziert.                                                                                                                                                                                                                 | Windows XP und höher    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | Eine beliebige gültige LCID                                                | Die LCID, die die Sprache der internationalen Version des Indexers identifiziert. Der Standardwert ist 1033 (en-US).                                                                                                                                                            | Windows XP und höher    |
| [Breadcrumb)](-search-3x-wds-qryidx-crumb.md)                     | AQS-Anweisung                                                 | Dieses Argument schränkt den Bereich ein, der durchsucht wird. In Windows Vista und höher unterstützt Search-MS vollständige AQS sowie eine spezielle Implementierung für ein `location` Argument. In Windows XP unterstützt Search-MS auch vollständige AQS, mit Ausnahme einer speziellen Implementierung von `kind` und `store` . | Windows XP und höher    |
| [Syntax](-search-3x-wds-qryidx-syntaxargument.md)           | NQS, AQS (Groß-/Kleinschreibung nicht beachtet)                                 | Die Abfrage Syntax, die zum Durchsuchen des Indexes verwendet werden soll: entweder natürliche Abfrage Syntax oder Erweiterte Abfrage Syntax (AQS). AQS ist die Standardeinstellung und wird immer als analysiert und unterstützt angenommen.                                                                                                    | Windows Vista und höher |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | Eine beliebige gültige Eigenschaft aus dem Eigenschaften System.                   | Eine-Eigenschaft, die die Spalte angibt, nach der die Ergebnisse gestapelt werden.                                                                                                                                                                                                                  | Windows Vista und höher |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | Ein vollständig angegebener Pfad für eine gespeicherte Suchdatei ( \* . Search-MS) | Die Ergebnisse der Unterabfrage werden als Quelle für die Abfrage verwendet. Das heißt, dass die Abfrage Begriffe anhand der Ergebnisse der Unterabfrage gesucht werden.                                                                                                                           | Windows Vista und höher |
| displayname                                                  | URL-codierte Zeichenfolge                                            | Der Name der aktuellen Suche.                                                                                                                                                                                                                                            | Windows Vista und höher |


Weitere Informationen finden Sie unter [Registrieren einer Anwendung in einem URL-Protokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)).

## <a name="examples"></a>Beispiele

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>Zugehörige Themen

[Locale-bezeichnerargumente](-search-3x-wds-qryidx-localeidentifiers.md)

[Crumb-Argument](-search-3x-wds-qryidx-crumb.md)

[Syntax Argument](-search-3x-wds-qryidx-syntaxargument.md)

[Stackedby-Argument](-search-3x-wds-qryidx-stackedby.md)

[Unterabfrage Argument](-search-3x-wds-qryidx-subquery.md)
