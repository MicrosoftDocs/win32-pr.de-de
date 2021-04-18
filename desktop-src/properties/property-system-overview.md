---
description: Das Windows-Eigenschaften System ist ein erweiterbares Lese-/Schreibsystem mit Daten Definitionen, das eine einheitliche Methode zum Ausdrücken von Metadaten über shellelemente bietet.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Übersicht über das Eigenschaftensystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab3a17eacdbaa9a5d0255004ba544b7c3f7ff2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347086"
---
# <a name="property-system-overview"></a>Übersicht über das Eigenschaftensystem

Das Windows-Eigenschaften System ist ein erweiterbares Lese-/Schreibsystem mit Daten Definitionen, das eine einheitliche Methode zum Ausdrücken von Metadaten über shellelemente bietet. Mit dem Windows-Eigenschaften System in Windows Vista und höher können Sie Metadaten für shellelemente speichern und abrufen. Ein shellelement ist ein beliebiges einzelnes Element, z. b. eine Datei, ein Ordner, eine e-Mail oder ein Kontakt. Eine Eigenschaft ist ein einzelner Metadatenelement, das einem shellelement zugeordnet ist. Eigenschaftswerte werden als [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur ausgedrückt.

Dieses Thema ist wie folgt organisiert:

-   [Introduction (Einführung)](#introduction)
-   [Entwicklungsszenarien](#development-scenarios)
-   [Eigenschaften und Windows Search](#properties-and-windows-search)
-   [Hinweis für Implementierer](#note-to-implementers)
-   [Dokumentation zu Windows-Eigenschaften System](#windows-property-system-documentation)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Eigenschaften werden durch ihren kanonischen Namen (z. b. `System.Document.LastAuthor` ) und den Eigenschafts Schlüssel (z `PKEY_Document_LastAuthor` . b.) eindeutig identifiziert. Ein Eigenschafts Schlüssel (pkey) ist der Namensteil eines Name-Wert-Paars, der aus einem pkey/PROPVARIANT-oder einer String/PROPVARIANT besteht, wobei die Zeichenfolge der kanonische Name des pkey (z `System.Document.LastAuthor` . b.) ist. Bei einem pkey handelt es sich um eine Definition, die dem Eigenschaften System alle Informationen über die Eigenschaft mitteilt, während der Wert eine tatsächliche Instanz der Eigenschaft ist. Ein pkey enthält intern eine FormatID und PROPID.

Eine einzelne Eigenschaft besteht aus den folgenden drei Teilen:

-   Ein kanonischer Name, z `System.Music.Artist` . b..
-   Eine Schema Beschreibung, die im XML-Dateiformat. PropDesc angegeben und Programm gesteuert über [**ipropertydescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription)ausgedrückt wird.
-   Ein-Wert, z. b. der Name eines Sängers.

Die Schema Beschreibung besteht aus Informationen über die Eigenschaft, z. b. den Eigenschaftsnamen, den Datentyp, Einschränkungen, Informationen darüber, wie die Eigenschaft mit Sichten und dem Suchsystem interagiert, usw. Der Name und die Schema Beschreibung werden global definiert und sind für alle Elemente und Typen identisch. Ein-Wert ist spezifisch für ein einzelnes Element. Das heißt, die `System.Music.Artist` Eigenschaft wird immer als mehrwertige Zeichenfolge definiert, kann jedoch für jedes Element einen anderen Wert (oder gar keinen Wert) haben.

Ein Eigenschafts Handler übersetzt in einer Datei gespeicherte Daten in ein strukturiertes Schema, das von erkannt wird und auf das Windows-Explorer, Windows Search und andere Anwendungen zugreifen können. Diese Systeme können dann mit dem Eigenschaften Handler interagieren, um Eigenschaften in die Datei zu schreiben und diese zu lesen. Die übersetzten Daten werden Programm gesteuert verfügbar gemacht und dem Benutzer über den Windows-Explorer in einer Vielzahl von Kontexten angezeigt, einschließlich der Detailansicht, der Infotipps, des Detail Bereichs, der Eigenschaften Seiten usw. Jeder Eigenschaften Handler ist einem bestimmten Dateityp zugeordnet, der durch die Dateinamenerweiterung gekennzeichnet wird. Entwickler sollten einen Eigenschafts Handler implementieren, der das systemeigene Format des Dateityps erzeugt und nutzt, z. b. jpg oder PNG, oder den In-Memory-Eigenschaften Speicher verwenden, der das binäre MS-propstore-Format erzeugt und nutzt.

Das Windows-Eigenschaften System erstellt ein abstraktes Datenmodell, das eine Abstraktions Ebene aus einzelnen Dateiformaten bereitstellt. Das abstrakte Datenmodell, das vom Windows-Eigenschaften System bereitgestellt wird, ist eine Methode zum Lesen und Schreiben eines erweiterbaren Satzes von benannten Werten, die einem shellelement zugeordnet sind. Der Value-Ausdruck ist flexibel und unterstützt zahlreiche Datentypen, und ist erweiterbar, sodass beliebige Daten (**VT- \_ BLOB**) und Objekte als Wert ausgedrückt werden können.

Aufgrund der Abstraktion können Sie die Attribute oder Metadaten eines beliebigen Elements Abfragen. Beispiele für Elemente, die abstrahiert werden können, sind Microsoft Office Dokumente, ID3-Tags und AutoCAD und andere proprietäre Software von Drittanbietern. Wenn Sie über eine JPEG-Datei verfügen, können Sie auch die JPEG-und EXIF-Codecs verwenden, um die Bytes der Datei zu lesen und zu ermitteln, was die Abmessungen des Bilds sind. Wenn Sie stattdessen über eine PNG-Datei verfügen, benötigen Sie einen anderen Codec und einen anderen Code. Durch die Verwendung des Windows-Eigenschaften Systems wird diese Art von Problem vermieden. Wenn Sie einen neuen Dateityp implementieren, haben Sie die Möglichkeit, die vom Windows-Eigenschaften System angebotene einheitliche Abstraktion einzuschließen und anzugeben, wie die Metadaten nutzbar gemacht werden sollen. Aus diesen Gründen ist es immer vorzuziehen, die vom Windows-Eigenschaften System bereitgestellte allgemeine Plattform zu verwenden.

## <a name="development-scenarios"></a>Entwicklungsszenarien

Eigenschaften werden von Produzenten und Consumern ausgedrückt. In diesem Zusammenhang sind Producer die Erfinder der Eigenschaften im Windows-Eigenschaften System, und Consumer sind Anwendungen (und Ihre Entwickler), die Eigenschafts Informationen von diesem System nutzen. Die Verwendung von-und-Teilnehmern im Windows-Eigenschaften System ist in der folgenden Tabelle aufgeführt.



| Verwendung des Windows-Eigenschaften Systems                                                                                                                                                                                            | Teilnehmer |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Ein Baustein, der eine erweiterbare Registrierung von Eigenschafts Beschreibungen, eine in-Memory-Eigenschaften Speicher Implementierung und Dienste zum Binden an Eigenschaften Handler, zum Umrechnen von Typen und zum Serialisieren von Eigenschaften speichern bereitstellt. | Consumer    |
| Anwendungen, die Eigenschaften auf abstrakte Weise lesen und schreiben möchten.                                                                                                                                                       | Consumer    |
| Eigenschaften Erfinder, die neue Eigenschaften für das Eigenschaften System definieren, indem Sie benutzerdefinierte Eigenschafts Schemas definieren und eigene Eigenschaften Handler entwickeln.                                                                          | Producer    |
| Dateiformat Besitzer, die den Zugriff auf die Eigenschaften aktivieren möchten, die in Ihren benutzerdefinierten Dateiformaten gespeichert werden.                                                                                                                           | Producer    |



 

Consumer nutzen vorhandene Eigenschaften, Schemas und Eigenschafts Handler. Zu den verfügbaren Eigenschaften gehören Lese-/Schreibeigenschaften von Eigenschaften Handlern für unterstützte Dateitypen und können auch einige benutzerdefinierte Eigenschaften enthalten. Zu den verfügbaren Schemas gehören mindestens das System Schema und manchmal auch andere. Ein Consumer kann eine Anwendung erstellen, um Metadaten zu nutzen und eine Ansicht basierend auf dem Künstler zu erstellen, unabhängig von den Ordnern, in denen die Elemente gespeichert sind. Die Datei Ordnerhierarchie ist irrelevant. Beispielsweise können Sie alle Lied Elemente eines bestimmten Sängers angeben, ohne sich Gedanken über den Speicherort dieser Elemente machen zu müssen. Dieses komplexe End-to-End-Szenario ist nicht auf das Windows-Eigenschaften System beschränkt, sondern umfasst mehrere verschiedene Komponenten, z. b. die Indizierungs-und Suchordner.

Eigenschaften Erfinder oder Entwickler von Drittanbietern sind Producer im Windows-Eigenschaften System. Wenn Sie die Definition einer neuen Eigenschaft vorbereiten, überprüfen Sie zunächst den Satz von Eigenschaften, den Windows definiert. Wenn Sie ein solches finden, das Ihren Anforderungen entspricht, verwenden Sie die-Eigenschaft und die Semantik, die der erforderlichen Verwendung entsprechen. verwenden Sie diese Eigenschaft nicht, und erfinden Sie keine neue. Wenn Sie eine neue benutzerdefinierte Eigenschaft definieren, versuchen Sie, eine Vereinbarung mit anderen Entwicklern zu erhalten, die Sie verwenden möchten, und das Ergebnis dieser Vereinbarung zu veröffentlichen, damit Sie der Benutzer Community dieser Eigenschaft beitreten können.

Producer können die Vorteile der Windows Explorer-Funktionalität nutzen. Wenn Sie z. b. ein neues Bildformat schreiben und einen Eigenschafts Handler implementieren, wird das neue Dateiformat in Windows-Explorer verfügbar. Benutzer können dann Ihre Fotos markieren und ihre Auflistung von Fotos basierend auf einer beliebigen Eigenschaft im Windows-Eigenschaften System pivotieren. Tatsächlich kann alles, was die Shell mit Eigenschaften vornimmt, Entwickler von Drittanbietern in ihren eigenen Anwendungen ausführen. Dies schließt das Gruppieren, sortieren, Abfragen und Anzeigen von vollständigen Eigenschaften ein. Der Benutzer, den Windows Explorer bereitstellt, kann größtenteils von Drittanbietern mit öffentlich verfügbaren APIs implementiert werden. Windows-Explorer kann mithilfe dieser APIs ersetzt oder erweitert werden.

Aus der Sicht einer Anwendung, die das Shell-Datenmodell verwendet, gibt es eine Vielzahl von Szenarios, in denen die Verwendung des Windows-Eigenschaften Systems beteiligt ist. Medien Verwaltungs Anwendungen sind ein hervorragendes Beispiel. Zu den Kerneigenschaften System Szenarios zählen Szenarien wie das Lesen der Schlüsselwort Eigenschaft eines Fotos oder das Festlegen der DateTaken-Eigenschaft. Beispiele für End-to-End-Integrationsszenarien, die vom Windows-Eigenschaften System aktiviert werden, für die jedoch mehrere andere Komponenten erforderlich sind, einschließlich der Anzeige aller Bilder oder der Suche nach einem Dokument, das ein Schlüsselwort enthält.

## <a name="properties-and-windows-search"></a>Eigenschaften und Windows Search

Eigenschaften dienen Producer und Consumern, wenn Sie mit der Windows-Suche und-Indizierung in eine Schnittstelle Windows Search verfügt über einen Cache mit Eigenschafts Werten, die in der Implementierung des Windows-Suchdienst (WSS) verwendet werden. Diese Eigenschaftswerte können Programm gesteuert mithilfe des Windows Search-OLE DB Anbieters oder mithilfe von [**isearchfolderitemfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)abgefragt werden, das Elemente in Suchergebnissen und Abfrage basierten Sichten darstellt. Windows Search sammelt und speichert dann Eigenschaften, die von Filter Handlern oder Eigenschaften Handlern ausgegeben werden, wenn ein Element wie ein Word-Dokument indiziert wird. Dieser Speicher wird verworfen und neu erstellt, wenn der Index neu erstellt wird.

> [!Note]  
> Beachten Sie Folgendes: Wenn Sie ein Schema erneut registrieren, werden Änderungen, die an Attributen von zuvor definierten Eigenschaften vorgenommen wurden, möglicherweise vom Indexer nicht beachtet. Die Lösung besteht darin, den Index neu zu erstellen oder neue Eigenschaften einzuführen, die die Änderungen widerspiegeln, anstatt alte zu aktualisieren (nicht empfohlen). Weitere Informationen finden Sie weiter unten in diesem Thema [unter Hinweise zu Implementierern](#note-to-implementers) .

 

Beispielsweise möchte ein Entwickler, der eine Medien Anwendung erstellt, Benutzern der Anwendung alle verfügbaren Musik von einem bestimmten Künstler anzeigen. Die Anwendung bietet dem Benutzer eine Liste der verfügbaren Künstler und generiert dann eine Liste aller verfügbaren Musik, die vom Benutzer ausgewählt wird. Oder ein Endbenutzer möchte eine Abfrage für? Artist: Beethoven? durchführen und für die vollständige Liste der verfügbaren Eigenschaften im Verlauf der Searche offengelegt werden. Dieses Beispiel umfasst die Verwendung des Shell-Namespace, der Eigenschaften Handler und/oder das Abfragen des Indexes über eine der folgenden Aktionen:

-   Eine shelldatenquelle.
-   Ein OLE DB-Anbieter.
-   Eine gespeicherte Suchdatei (. Search-MS), die verwendet wird, um eine Abfrage zu initiieren, indem Sie zur Suchdatei in Windows-Explorer navigiert oder Programm gesteuert an [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) gebunden wird.

> [!Note]  
> Obwohl die `System.Kind` Eigenschaft nicht an diesem Medien Anwendungsszenario teilnimmt, könnte Sie verwendet werden, um eine Abfrage zu erstellen, die alle. Search-MS-Dateien in einem bestimmten Bereich zurückgibt.

 

Die bevorzugte Methode für den Zugriff auf die Such-APIs und die Erstellung von Windows Search-Anwendungen ist die Verwendung einer shelldatenquelle. [**Isearchfolderitemfactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) ist eine Komponente, mit der Instanzen der Suchordner-Datenquelle erstellt werden können. Dies ist eine Art "virtuelle" Datenquelle, die von der Shell bereitgestellt wird, die Abfragen für andere Datenquellen im Shellnamespace ausführen und Ergebnisse aufzählen kann. Dies kann entweder mithilfe des Indexers oder durch manuelles auflisten und Überprüfen von Elementen in den angegebenen Bereichen durchlaufen werden.

Entwickler von Drittanbietern können Anwendungen erstellen, die die Daten im Index über programmgesteuerte Abfragen nutzen, und die Daten im Index erweitern, damit benutzerdefinierte Datei-und Elementtypen von Windows Search indiziert werden. Wenn Sie Abfrageergebnisse in Windows-Explorer anzeigen möchten, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler zum Erweitern des Indexes erstellen können. Wenn allerdings alle Abfragen Programm gesteuert werden (z. b. über OLE DB) und vom Anwendungscode und nicht von der Shell interpretiert werden, wird ein Shellnamespace weiterhin bevorzugt, ist aber nicht erforderlich. Ein Protokollhandler ist erforderlich, damit Windows Informationen zum Inhalt der Datei, z. b. Elemente in Datenbanken oder benutzerdefinierten Dateitypen, abrufen kann. Obwohl Windows Search den Namen und die Eigenschaften der Datei indizieren kann, enthält Windows keine Informationen zum Inhalt der Datei. Folglich können solche Elemente in der Windows-Shell nicht indiziert oder verfügbar gemacht werden. Durch Implementieren eines benutzerdefinierten Protokoll Handlers können Sie diese Elemente verfügbar machen. Eine Liste der Handler, die von dem Entwickler Szenario identifiziert werden, das Sie zu erreichen versuchen, finden Sie unter "Übersicht über Handler" in der [Windows-Suche als Entwicklungsplattform](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Eine shelldatenquelle wird manchmal als Shellnamespace Erweiterung bezeichnet. Ein Handler wird manchmal als Shellerweiterung oder Shellerweiterungs Handler bezeichnet.

 

## <a name="note-to-implementers"></a>Hinweis für Implementierer

Aufgrund möglicher Schwierigkeiten, die der Indexer bei der Verwendung des Schema Schema des Eigenschaften Systems aufweisen kann, ist es wichtig, Attribute sorgfältig und strategisch für die erste Version des Schemas zu definieren. Alle Änderungen an Attributen (Typ, Spaltenbreite, ggf.) werden in der Datenbank nach der Registrierung eines Schemas nicht wiedergegeben. Die einzigen Möglichkeiten, diese Änderungen zu erkennen, nachdem das Schema einmal auf einem System registriert wurde, würden entweder den Index neu erstellen und dann das neue Schema registrieren oder das Schema registrieren und dann für jede nachfolgende Version eine neue Eigenschaft erstellen. beispielsweise `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` usw. Es wird nicht empfohlen, neue Eigenschaften auf diese Weise zu erstellen, da sich mehrere überflüssige Spalten möglicherweise auf die Systemleistung auswirken.

## <a name="windows-property-system-documentation"></a>Dokumentation zu Windows-Eigenschaften System

Der Rest dieser Dokumentation enthält die folgenden Abschnitte:

-   [Entwicklerhandbuch für Windows-Eigenschaften System](property-system-developer-s-guide.md)

    Beschreibt ausführlich, wie die wichtigsten Entwicklungsszenarien mithilfe des Windows-Eigenschaften Systems implementiert werden.

-   [Eigenschaften System Referenz](property-system-reference.md)

    Dokumentiert die [Fenster Eigenschaften](props.md), [das Eigenschafts Beschreibungs Schema](property-description-schema.md), [Schnittstellen](interfaces.md), [Funktionen](functions.md), [Strukturen](structures.md), [Konstanten, Enumerationen und Flags](constants--enumerations--and-flags.md) des Windows-Eigenschaften Systems.

-   [Eigenschaftensystem-Codebeispiele](property-system-code-samples.md)

    Beschreibt Beispiele, die veranschaulichen, wie das Windows-Eigenschaften System verwendet wird.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zur Wiederverwendung des In-Memory-Eigenschaften Speicher finden Sie unter [Initialisieren von Eigenschaften Handlern](building-property-handlers-property-handlers.md) und [**pscreatememorypropertystore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Eine Spezifikation des Binärdatei Formats von Microsoft Property Store finden Sie unter [ \[ MS \_ propstore \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   Die Beziehung zwischen der Windows-Suche und-Indizierung und der Erweiterung des Indexes werden in den folgenden Themen in Windows Search erläutert:
    -   [Entwickeln von Filter Handlern für Windows Search](../search/-search-ifilter-conceptual.md)
    -   [Entwickeln von Protokoll Handlern für Windows Search](../search/-search-3x-wds-phaddins.md)
    -   [Entwickeln von Eigenschaften Handlern für Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Informationen zum Herunterladen von Windows 7 oder zum aktualisierten Windows Vista SDK finden Sie in der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklerhandbuch für Windows-Eigenschaften System](property-system-developer-s-guide.md)
</dt> <dt>

[Eigenschaften System Referenz](property-system-reference.md)
</dt> <dt>

[Eigenschaftensystem-Codebeispiele](property-system-code-samples.md)
</dt> </dl>

 

 
