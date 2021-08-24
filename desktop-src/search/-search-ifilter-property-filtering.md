---
description: Eigenschaften werden mithilfe registrierter Eigenschaftenhandler oder mithilfe von Filtern, die für bestimmte Dateitypen registriert sind, aus Elementen extrahiert. Ein Filterhandler (eine Implementierung der IFilter-Schnittstelle) kann den Inhalt eines Dateityps auf verschiedene Weise interpretieren.
ms.assetid: 6701d151-c36f-43e5-929b-9831c5ce5823
title: Zurückgeben von Eigenschaften von einem Filterhandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1842710af65e22f5a730891ea6e7f32053b92212f8c3ad4c5f0f68f23578d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594854"
---
# <a name="returning-properties-from-a-filter-handler"></a>Zurückgeben von Eigenschaften von einem Filterhandler

Eigenschaften werden mithilfe registrierter Eigenschaftenhandler oder mithilfe von Filtern, die für bestimmte Dateitypen registriert sind, aus Elementen extrahiert. Ein Filterhandler (eine Implementierung der [**IFilter-Schnittstelle)**](/windows/win32/api/filter/nn-filter-ifilter) kann den Inhalt eines Dateityps auf verschiedene Weise interpretieren.

Dieses Thema ist wie folgt organisiert:

- [Eigenschaftenfilterung](#returning-properties-from-a-filter-handler)
  - [Größenbeschränkungen für Eigenschaften](#property-size-limitations)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="property-filtering"></a>Eigenschaftenfilterung

Bewährte Methoden für die Eigenschaftenfilterung sind in der folgenden Tabelle aufgeführt.

| Methode                                                | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFilter::Init**](/windows/win32/api/filter/nf-filter-ifilter-init)      | Gibt die [**IFILTER \_ FLAGS-Enumeration**](/windows/win32/api/filter/ne-filter-ifilter_flags) zurück. Wenn der *IFILTER \_ FLAGS \_ OLE \_ PROPERTIES-Member* dieser Enumeration auf eins festgelegt ist, verwendet Windows Search die [Schnittstellen IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) und [IPropertyStorage,](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) um externe Werttypeigenschaften aufzählen und darauf zu zugreifen. |
| [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) | Gibt Informationen aus einem Dokument in "Chunks" mit Blocktyp (Text oder Wert), Name und Locale zurück. Ein Block enthält eine Dokumenteigenschaft.                                                                                                                                                                                                                                                                                                      |
| [**IFilter::GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext)   | Ruft eine Texttypeigenschaft aus einem Block ab.                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) | Ruft eine Werttypeigenschaft aus einem Block ab.                                                                                                                                                                                                                                                                                                                                                                                                        |

Die folgende Abbildung zeigt ein Beispieldokument. Die eigenschaft external value-type (mithilfe der Methoden der `DocTitle` [Schnittstellen IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) und [IPropertyStorage)](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) und die interne Werttypeigenschaft (die als Ergebnis einer benutzerdefinierten IFilter-Implementierung ermittelt wurde) beschreiben das Dokument als `Book` Ganzes. [](/windows/win32/api/filter/nn-filter-ifilter) Die Texttypeigenschaften `Contents` und beschreiben den Inhalt des `Chapter` Dokuments. Bei der Verarbeitung dieses Dokuments identifiziert und extrahiert der Filterhandler (eine Implementierung der **IFilter-Schnittstelle)** diese Eigenschaften.

![Diagramm, das die Elemente eines typischen Dokuments zeigt](images/ifilterpropertyextraction.png)

### <a name="property-size-limitations"></a>Größenbeschränkungen für Eigenschaften

Es gibt zwei potenzielle Einschränkungen bei der Eigenschaftengröße:

- Die maximale Größe der Daten, die Windows Search akzeptiert, pro Datei.
- Die maximale Größe pro Eigenschaft, wie in der Eigenschaftenbeschreibungsdatei definiert.

Derzeit verwendet Windows Search nicht die definierte Eigenschaftsgröße, wenn die Menge der Daten berechnet wird, die von einem Element akzeptiert werden. Stattdessen ist das limit, Windows Search verwendet, das Produkt aus der Größe der Datei und der `MaxGrowFactor` (Dateigröße N \* MaxGrowFactor), die aus der Registrierung gelesen wird. Der Standardwert `MaxGrowFactor` ist vier.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Gathering Manager
            MaxGrowFactor
```

Wenn Ihr Dateityp tendenziell klein ist, aber größere Eigenschaften aufweist, akzeptiert Windows Search möglicherweise nicht alle Eigenschaftsdaten, die Sie aus geben möchten. Sie können jedoch erhöhen, `MaxGrowFactor` um Ihren Anforderungen gerecht zu werden.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf GitHub verfügbar [ist,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)veranschaulicht, wie eine IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle erstellt**](/windows/win32/api/filter/nn-filter-ifilter) wird.
- Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess](-search-indexing-process-overview.md).
- Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
- Informationen zum Abfragen von Dateiassoziationsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))
- Eine Übersicht über Eigenschaften und Eigenschaftenhandler sowie eine Liste der Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können, finden Sie unter [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)

[Informationen zu Filterhandlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filterhandlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Filterhandler, die mit Windows](-search-ifilter-implementations.md)

[Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)

[Testen von Filterhandlern](-search-ifilter-testing-filters.md)
