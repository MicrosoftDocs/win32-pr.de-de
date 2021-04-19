---
description: Eigenschaften werden aus Elementen mithilfe registrierter Eigenschaften Handler oder mithilfe von Filtern extrahiert, die für bestimmte Dateitypen registriert sind. Ein Filter Handler (eine Implementierung der IFilter-Schnittstelle) kann den Inhalt eines Dateityps auf verschiedene Arten interpretieren.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Zurückgeben von Eigenschaften aus einem Filter Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df0bfc811176e9b0672dbcbe4ef4f04f3c3a6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346498"
---
# <a name="returning-properties-from-a-filter-handler"></a>Zurückgeben von Eigenschaften aus einem Filter Handler

Eigenschaften werden aus Elementen mithilfe registrierter Eigenschaften Handler oder mithilfe von Filtern extrahiert, die für bestimmte Dateitypen registriert sind. Ein Filter Handler (eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) kann den Inhalt eines Dateityps auf verschiedene Arten interpretieren.

Dieses Thema ist wie folgt organisiert:

- [Eigenschaften Filterung](#returning-properties-from-a-filter-handler)
  - [Einschränkungen der Eigenschafts Größe](#property-size-limitations)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="property-filtering"></a>Eigenschaften Filterung

Die bewährten Methoden für die Eigenschaften Filterung sind in der folgenden Tabelle aufgeführt.

| Methode                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Gibt die [**IFilter- \_ Flags**](/windows/win32/api/filter/ne-filter-ifilter_flags) -Enumeration zurück. Wenn das *\_ \_ OLE \_ Properties* -Element der IFilter-Flags auf 1 festgelegt ist, verwendet Windows Search die Schnittstellen [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) und [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) Interface, um externe Werttyp Eigenschaften aufzulisten und darauf zuzugreifen. |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Gibt Informationen aus einem Dokument in "Blöcken" mit Segmenttypen (Text oder Wert), Name und Gebiets Schema zurück. Ein Block enthält eine Dokument Eigenschaft.                                                                                                                                                                                                                                                                                                      |
| [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Ruft eine Texttyp Eigenschaft aus einem Segment ab.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Ruft eine Werttyp Eigenschaft aus einem Segment ab.                                                                                                                                                                                                                                                                                                                                                                                                        |

Die folgende Abbildung zeigt ein Beispiel Dokument. Die Eigenschaft "externer Werttyp" `DocTitle` (abgerufen mithilfe der Methoden der Schnittstellen " [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) " und " [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ") und der Eigenschaft "interner Werttyp" `Book` (abgerufen als Ergebnis einer benutzerdefinierten [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Implementierung) beschreiben das Dokument als Ganzes. Die Texttyp Eigenschaften `Contents` und `Chapter` beschreiben den Inhalt des Dokuments. Bei der Verarbeitung dieses Dokuments identifiziert und extrahiert der Filter Handler (eine Implementierung der **IFilter** -Schnittstelle) diese Eigenschaften.

![Diagramm, das die Elemente eines typischen Dokuments anzeigt](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Einschränkungen der Eigenschafts Größe

Für die Eigenschaften Größe gibt es zwei mögliche Einschränkungen:

- Die maximale Größe der Daten, die von Windows Search pro Datei akzeptiert werden.
- Die maximale Größe pro Eigenschaft, wie in der Eigenschafts Beschreibungsdatei definiert.

Derzeit verwendet Windows Search die definierte Eigenschaften Größe nicht, wenn die Menge der Daten berechnet wird, die Sie von einem Element akzeptiert. Stattdessen ist der Grenzwert, den Windows Search verwendet, das Produkt der Dateigröße und der `MaxGrowFactor` (Dateigröße N \* MaxGrowFactor), die aus der Registrierung gelesen werden. Der Standardwert `MaxGrowFactor` ist vier.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Wenn Ihr Dateityp tendenziell klein ist, aber größere Eigenschaften hat, akzeptiert Windows Search möglicherweise nicht alle Eigenschaften Daten, die Sie ausgeben möchten. Sie können jedoch die `MaxGrowFactor` an Ihre Anforderungen anpassen.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".
- Eine Übersicht über Eigenschaften und Eigenschafts Handler sowie eine Liste der Systemeigenschaften, die Sie für die Dateiformate verwenden können, finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Informationen zu Filter Handlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
