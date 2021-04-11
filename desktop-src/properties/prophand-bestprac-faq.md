---
description: In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.
ms.assetid: E583A00B-F615-41c8-AECF-061F1396DB9A
title: Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5188e66f08f3c6cf449f8bc61feb6aac829d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218103"
---
# <a name="property-handler-best-practices-and-faq"></a>Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern

In diesem Thema wird erläutert, wie Sie Eigenschafts Handler erstellen und registrieren, um mit dem Windows-Eigenschaften System zu arbeiten.

Dieses Thema ist wie folgt organisiert:

-   [Bewährte Methoden](#property-handler-best-practices-and-faq)
    -   [Überschreiben von Datei System Eigenschaften](#overriding-file-system-properties)
    -   [Speichern von Eigenschaften in XML-basierten Dateiformaten](#storing-properties-in-xml-based-file-formats)
    -   [Berechnete Eigenschaften](#computed-properties)
-   [Häufig gestellte Fragen](#property-handler-best-practices-and-faq)
-   [Zugehörige Themen](#related-topics)

## <a name="best-practices"></a>Bewährte Methoden

Die hier beschriebenen bewährten Methoden bieten nützliche Implementierungs Tipps.

### <a name="overriding-file-system-properties"></a>Überschreiben von Datei System Eigenschaften

Einige Eigenschaften für Dateien werden von der Dateisystem-Datenquelle bereitgestellt, wie z. b.:

-   Pkey \_ filename
-   Pkey- \_ Erweiterung
-   Pkey- \_ Modifizierungszeit

Im Allgemeinen können Eigenschaften Handler keine Werte für diese Eigenschaften bereitstellen. In einigen Fällen können diese Eigenschaften jedoch auf der Grundlage von Registrierungsinformationen überschrieben werden, die vom Eigenschaften Handler bereitgestellt werden. Eigenschafts Handler füllen die **HKEY- \_ Klassen \_ root** \\ **CLSID** \\ *{Handler CLSID}* \\ **overridefilesystemproperties** mit den Namen von Eigenschaften auf, die Sie überschreiben möchten. Dies ist auf einen festgelegten Satz von Eigenschaften beschränkt, der in der folgenden Liste angezeigt wird, in der das System über Kenntnisse verfügt.

Das Überschreiben wird für die folgenden Eigenschaftswerte unterstützt:

-   [System. Kind](./props-system-kind.md)
-   [System. filename](./props-system-filename.md)
-   [System. ispinnedtonamespacetree](./props-system-ispinnedtonamespacetree.md)
-   [System.ItemNameDisplay](./props-system-itemnamedisplay.md)
-   [System. sfgaoflags](./props-system-sfgaoflags.md)
-   [System. itempathdisplay](./props-system-itempathdisplay.md)
-   [System. itempathdisplaynarrow](./props-system-itempathdisplaynarrow.md)
-   [System. itemfoldernamedisplay](./props-system-itemfoldernamedisplay.md)
-   [System. itemfolderpathdisplay](./props-system-itemfolderpathdisplay.md)
-   [System. itemfolderpathdisplaynarrow](./props-system-itemfolderpathdisplaynarrow.md)

Eine vollständige Liste aller Shelleigenschaften finden Sie unter [Shelleigenschaften](./props.md).

> [!IMPORTANT]
> Die überschriebenen Eigenschaftswerte werden nur verwendet, wenn die Dateien indiziert werden. Folglich werden durch das Durchsuchen von Dateien aus der Dateisystem-Datenquelle die überschriebenen Werte nicht offengelegt.

 

### <a name="storing-properties-in-xml-based-file-formats"></a>Speichern von Eigenschaften in XML-basierten Dateiformaten

Es stehen zwei grundlegende Optionen zum Speichern von Eigenschaften in XML-basierten Dateiformaten zur Verfügung:

-   Speichern Sie jede Eigenschaft gemäß dem XML-Schema des Dokuments mithilfe von XML-Elementen und Attributen. Diese Vorgehensweise ist eher "XML-freundlich".
-   Serialisieren Sie den gesamten Eigenschafts Speicher in ein BLOB (Binary Large Object), konvertieren Sie das BLOB in eine Base64-codierte Zeichenfolge, und speichern Sie diese Zeichenfolge dann in der XML-Datei. Dies ist die einfachere der beiden Ansätze und kann verwendet werden, um Unterstützung für geöffnete Metadaten zu bieten.

Einige Handler können diese Ansätze kombinieren und einige wichtige Werte im XML-Standardformat speichern und den Rest beispielsweise in einem BLOB speichern.

### <a name="computed-properties"></a>Berechnete Eigenschaften

Einige Eigenschaften werden von bestimmten Attributen einer Datei abgeleitet. Die [System. Image. Dimensions](./props-system-image-dimensions.md) -Eigenschaft wird z. b. durch die tatsächlichen Dimensionen des Bilds in einer Bilddatei bestimmt. Da diese Eigenschaftswerte nicht durch den Eigenschaften Handler geändert werden können, werden Sie `isInnate="true"` in der Eigenschafts Beschreibung gekennzeichnet. Andere Eigenschaften werden aus einem Teil einer bestimmten Eigenschaft oder durch aggregierten der Werte mehrerer Eigenschaften berechnet. Da Updates für diese "berechneten" Eigenschaften zu einer Mehrdeutigkeit bei der Änderung der "Source"-Werte führen, sollten berechnete Eigenschaften `isInnate="true"` in der Eigenschafts Beschreibung gekennzeichnet oder als schreibgeschützt gemeldet werden. Die zweite Option ist verfügbar, indem der Handler angewiesen wird, S \_ false aus [**ipropertystorecapabili:: ispropertywrite Table**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable)zurückzugeben.

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

In diesem Abschnitt finden Sie Antworten auf häufig gestellte Fragen zu Eigenschaften und Eigenschaften Handlern sowie begleitende Antworten.

-   **Frage:** Warum wird mein Eigenschaftenhandler nicht vom Windows Search-Indexer geladen?

    Der Indexer für Windows-Suche wird als Systemdienst ausgeführt und kann keine DLLs laden, die im Benutzerprofil Verzeichnis gespeichert sind. Wenn Sie mit Microsoft Visual Studio erstellen und Debuggen, wird die dll in Ihrem Benutzerprofil abgelegt (und wird daher nicht vom Indexer geladen). Um dieses Problem zu umgehen, kopieren Sie die dll außerhalb Ihres Profilordners (z. **b. in C: \\ Programme \\ yourappname**), und registrieren Sie Sie dort.

    Genauere Anleitungen zum Entwickeln von Eigenschaften Handlern für die Verwendung des Windows Search-Indexers finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md).

-   **Frage:** Welche Eigenschaften sollten über die Enumerationsmethoden [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) und [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) gefunden werden?

    Nicht alle Clients von Eigenschaften Speicher Objekten verwenden diese Methoden. Einige Clients sind mit den Eigenschaften vertraut, die Sie direkt (anhand des pkey-namens) anfordern möchten, oder Sie erhalten Eigenschafts Informationen über eine Eigenschaften Beschreibungs Liste. Die Eigenschaften Ermittlungsmethoden unterstützten verschiedene andere Szenarien. Wenn eine Eigenschaft nicht an diesen Szenarien teilnehmen muss, muss Sie nicht aufgezählt werden. Daher kann ein Eigenschaften Handler einen nicht-VT- \_ Wert für Eigenschaften, die nicht durch die [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) -Methode und die [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) -Methode ermittelt werden, als nicht-VT-Wert ausgeben.

    Eigenschaften sollten jedoch über diese Methoden sichtbar sein, wenn eine der folgenden Bedingungen erfüllt ist:

    -   **Wenn die Eigenschaft indiziert ist, sodass Sie durchsuchbar ist:** Dies bedeutet, dass Sie in den Windows Search-Eigenschaften Speicher (angegeben durch `isColumn = "true"` im Eigenschafts Beschreibungs Schema) oder für voll Text suchen ( `inInvertedIndex = "true"` ) enthalten ist. Wenn diese Flags fehlen oder keine Eigenschafts Beschreibung vorhanden ist, werden die Eigenschaften des Typs "String" automatisch dem umgekehrten Index hinzugefügt, um die Suche zu aktivieren. Da die Liste bekannter Eigenschaften (mit Beschreibungen der installierten Eigenschaften) im Eigenschaften System sehr groß ist (mehr als 800 Eigenschaften), wäre es unpraktisch, jeden Eigenschaften Handler für jede im Eigenschaften System registrierte Eigenschaft zu Fragen. Stattdessen zählt der Indizierungsprozess die relevanten Eigenschaften aus dem Eigenschaften Handler für jedes Element auf, das er indiziert, und verwendet die Werte der enumerationseigenschaften, um den Volltextindex zu erstellen.
    -   **Wenn die Eigenschaft kopiert werden soll, wenn der Eigenschaften Satz des Elements dupliziert wird:** Um die Funktion "Eigenschaften Satz kopieren" zu implementieren, werden die Eigenschaften, die kopiert werden sollen, durch die [**IPropertyStore:: GetCount**](/previous-versions/windows/desktop/legacy/bb761472(v=vs.85)) -Methode und die [**IPropertyStore:: GetAt**](/previous-versions/windows/desktop/legacy/bb761471(v=vs.85)) -Methode sichtbar. Eigenschaften, die nicht kopiert werden müssen oder nicht sinnvoll sind, sollten nicht eingeschlossen werden.
    -   **Wenn der Eigenschafts Wert nicht leer ist (VT \_ Empty):** Eigenschaftswerte, die leer sind, sind für Clients nicht nützlich. Wenn Clients versuchen, leere Eigenschaftswerte zurückzugeben, wird der Wert "VT \_ empty" zurückgegeben. Daher sollten Eigenschaften mit leeren Werten nicht aufgezählt werden.
    -   **Wenn die Eigenschaft entfernt werden soll, wenn die Funktion "Remove Properties" aufgerufen wird:** Diese Funktion ist zum Schutz des Datenschutzes vorhanden. er ermittelt alle Werte aus dem Eigenschafts Handler über die Enumeration und entfernt alle, die vom Benutzer zum Entfernen ausgewählt wurden.
        > [!Note]  
        > Beim Aufzählen von Eigenschaften wird die Gruppe von Eigenschaften, die von einem bestimmten Eigenschaften Handler unterstützt werden, nicht kommuniziert, wenn der Handler ein festes Schema (und nicht geöffnete Metadaten) unterstützt. Stattdessen sollten solche Handler den Satz von Eigenschaften dokumentieren, die Sie unterstützen.

         

-   **Frage:** Gewusst wie Sie wissen, welche Dateiformate offene Metadaten unterstützen?

    Weitere Informationen zur Unterstützung offener Metadaten finden Sie unter "Dateitypen, die offene Metadaten unterstützen" in [Dateitypen](../shell/fa-file-types.md).

-   **Frage:** Können VT \_ NULL-Werte mithilfe eines Eigenschaften Handlers gespeichert werden?

    Nein. \_Die NULL-Werte von VT werden \_ bei Aufrufen von [**IPropertyStore:: GetValue**](/previous-versions/windows/desktop/legacy/bb761473(v=vs.85)) und [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))in VT Empty konvertiert.

-   **Frage:** Welche Datums Zeichen folgen Formate werden von der [**propvariantchangetype**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) -Funktion unterstützt?

    Im Allgemeinen sollten Eigenschaften, die Datums-/Uhrzeitwerte darstellen, mithilfe von VT \_ FILETIME dargestellt werden. Viele Datenquellen stellen diese Informationen jedoch in Form von Zeichen folgen dar. Die hilfsapi [**propvariantchangetype**](/windows/win32/api/propvarutil/nf-propvarutil-propvariantchangetype) unterstützt das Umwandeln einiger Zeichen folgen Datumsformate in [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Werte, wie in der folgenden Tabelle gezeigt.

    

    | Format                  | Windows Vista, Windows XP und Microsoft Windows-Desktop Suche (WDS) | Windows 7 | Notizen                                                                                                                                                                                                 |
    |-------------------------|-----------------------------------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | yyyy/mm/dd: hh: mm: SS. uuu | Ja                                                                   | Ja       | UTC y = Jahr, m = Monat, d = Datum, h = Stunden (24-Stunden-Takt), m = Minuten, s = Sekunden, u = Mikrosekunden                                                                                                           |
    | yyyy-mm-ddThh: mm: SSZ    | Nein                                                                    | Ja       | **ISO8601-Format Spezifikation** UTC (angegeben durch den "Z"-Zeit Zonen Indikator); y = Jahr, m = Monat, d = Datum, h = Stunden (24-Stunden-Takt), m = Minuten, s = Sekunden; 'T ' ist ein Trennzeichen für den Uhrzeit Teil.<br/> |

    

     

-   **Frage:** Ist es möglich, einen schreibgeschützten Eigenschaften Handler zu erstellen?

    Ja. Einige eigenschaftenhandlerimplementierungen unterstützen nicht das Schreiben von Eigenschafts Werten. Diese Eigenschaften Handler sollten STGM \_ E \_ AccessDenied bei Aufrufen von **iinitializexxx:: Initialize** zurückgeben, die "STGM- \_ Lese schreiben" oder bei jedem Aufruf von " [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))" übergeben.

    Alle im STGM-Lesemodus geöffneten Eigenschaften Handler \_ sollten \_ \_ bei Aufrufen von [**IPropertyStore:: SetValue**](/previous-versions/windows/desktop/legacy/bb761475(v=vs.85))STGM E AccessDenied zurückgeben.

-   **Frage:** Kann ein Eigenschaften Handler eine Eigenschaft als schreibgeschützt behandeln, auch wenn das Schema angibt, dass die Eigenschaft beschreibbar ist?

    Ja. Im Schema System werden Eigenschaften schreibgeschützt (einschließlich derjenigen mit `isInnate = "true"` ) oder Lese-/Schreibzugriff. Eigenschaften Handler, die das Schreiben einer bestimmten Eigenschaft, die das Schema besagt, nicht unterstützen, sollten [**ipropertystorecapabilitäten**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities) implementieren und \_ bei Aufrufen von [**ipropertystorecapabili:: ispropertywritable**](/windows/win32/api/propsys/nf-propsys-ipropertystorecapabilities-ispropertywritable) für diese Eigenschaft den Wert "false" zurückgeben. Dies gibt an, dass die Eigenschaft im Kontext dieses Handlers und dieser Datei nicht beschreibbar ist.

    > [!Note]  
    > Die umgekehrte Aktion ist nicht möglich. Sie können einen Eigenschafts Handler nicht aktivieren, um eine Eigenschaft zu schreiben, die im Schema als schreibgeschützt gekennzeichnet ist.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegendes zu Eigenschaften Handlern](./building-property-handlers-properties.md)
</dt> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
</dt> </dl>

 

 
