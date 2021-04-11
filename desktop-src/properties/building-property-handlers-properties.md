---
description: Eigenschaften werden durch IDs dargestellt, die als Eigenschaften Bezeichner (PIDs) bezeichnet werden.
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Grundlegendes zu Eigenschaften Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564d6f8bd325e649ff1356869932521d8c1cd885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215403"
---
# <a name="understanding-property-handlers"></a>Grundlegendes zu Eigenschaften Handlern

Eigenschaften werden durch IDs dargestellt, die als Eigenschaften Bezeichner (PIDs) bezeichnet werden. Jede Eigenschaft muss über eine Globally Unique Identifier (GUID) verfügen. Dieser Bezeichner besteht aus einer GUID, die eine Auflistung von Eigenschaften darstellt, die als Eigenschaften Satz bezeichnet werden, sowie eine Zeichenfolge oder eine 32-Bit-Ganzzahl, um die Eigenschaft innerhalb der Menge zu identifizieren. Wenn die ganzzahlige Form von ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig eingestuft. Anbieter können garantieren, dass ihre Eigenschaften eindeutig definiert werden, indem Sie in einem Eigenschaften Satz platziert werden, der durch ihre eigenen GUIDs definiert ist.

> [!IMPORTANT]
> Es ist wichtig, dass Sie Eigenschaften sorgfältig und strategisch für die erste Version des Schemas definieren. Änderungen an benutzerdefinierten Eigenschaften (z. b. Spaltenbreite oder Eigenschaftentyp) werden nach der Registrierung eines Schemas nicht in der Datenbank berücksichtigt. Die einzige Möglichkeit, diese Änderungen zu erkennen, nachdem das Schema einmal in einem System registriert wurde, besteht darin, den Index neu zu erstellen, das neue Schema zu registrieren, oder das Schema zu registrieren und dann eine neue Eigenschaft (die aus einem kanonischen Namen und einem pkey besteht) für jede untergeordnete Version zu erstellen; beispielsweise `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` usw.). Es wird nicht empfohlen, neue Eigenschaften auf diese Weise zu erstellen, da sich mehrere überflüssige Spalten möglicherweise auf die Systemleistung auswirken.

 

Dieses Thema ist wie folgt organisiert:

-   [Metadaten](#metadata)
    -   [Open Metadata](#open-metadata)
-   [Informationen zu Eigenschaften Handlern](#about-property-handlers)
-   [Legacy Technologie](#legacy-technology)
-   [Zugehörige Themen](#related-topics)

## <a name="metadata"></a>Metadaten

In Windows Vista und höher ist ein neues Eigenschaften System, das auf Metadaten basiert, für die Organisation von Elementen, z. b. Dateien, e-Mails und Kontakten, von zentraler Bedeutung. In diesem neuen Eigenschaften System können Elemente basierend auf Ihren Metadaten durchsucht werden, und Benutzer können diese Metadaten lesen oder schreiben. Metadaten in diesem System werden durch einen erweiterbaren Satz von *Eigenschaften* dargestellt, die als Name/Wert-Paare implementiert werden.

In Windows Vista und höher deckt eine umfangreiche Sammlung von Eigenschaften die Besonderheiten von Elementen wie Fotos, Musik, Dokumenten, Nachrichten, Kontakten und Dateien ab. Unabhängige Softwarehersteller (Independent Softwareanbieters, ISVs) können Ihre eigenen Eigenschaften für die Plattform einführen, wenn keine vorhandene Eigenschaft Ihren Anforderungen entspricht.

### <a name="open-metadata"></a>Open Metadata

Das Eigenschaften System in Windows Vista und höher ist ein offenes Metadatensystem. Ein Dateiformat speichert alle ihm zugewiesenen Eigenschaften und macht diesen Wert unabhängig von ihrer Relevanz oder Bedeutung verfügbar. Dadurch können Entwickler von Drittanbietern zusätzliche Eigenschaften an die Datei anfügen, ohne dass eine Änderung im zugeordneten Eigenschaften Handler erforderlich ist. Open Metadata ist ein leistungsfähiges Konzept. Weitere Informationen zur Unterstützung offener Metadaten für ein XML-basiertes Dateiformat finden Sie unter "unterstützen offener Metadaten" in [Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md).

> [!Note]  
> Eigenschaften Handler sind immer bestimmten Dateitypen zugeordnet. Wenn das Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaften Handler erfordern, sollten Sie daher immer eine eindeutige Dateinamenerweiterung für jedes Dateiformat registrieren.

 

## <a name="about-property-handlers"></a>Informationen zu Eigenschaften Handlern

In Windows Vista und höher verfügt Windows über ein erweiterbares Eigenschaften System zum Speichern und Abrufen von Metadaten in den Dateien und Datenelementen, auf die Sie zugreifen. Windows-Explorer und das Windows-Suchsystem verwenden zusammen mit anderen Anwendungen Eigenschafts Handler, um diese Metadaten zu lesen und zu ändern. Wenn Sie ein Entwickler sind, der Besitzer eines bestimmten Dateityps ist, sollten Sie einen Eigenschaften Handler registrieren, um dem Eigenschaften System den Zugriff auf die Metadaten in Ihren Dateien zu geben. In einigen Fällen können Sie möglicherweise einen vorhandenen Eigenschaften Handler verwenden, der das Dateiformat und seine Eigenschaften lesen und verstehen kann. in anderen Fällen müssen Sie möglicherweise einen neuen Eigenschaften Handler für den Dateityp entwickeln.

Der erste Schritt beim Schreiben eines Eigenschaften Handlers besteht darin, die vom Dateityp unterstützten Eigenschaften zu überprüfen. Eigenschaftswerte werden im Dateistream gespeichert, hauptsächlich, um die Übertragbarkeit zu ermöglichen. Wenn die Eigenschaftswerte in der Datei selbst gespeichert werden, wie Sie in diesem System vorhanden sind, kann ein Benutzer eine Datei auf einen anderen Computer, ein USB-Speicherstick oder ein anderes Dateisystem kopieren oder die Datei als e-Mail-Anlage senden, die Eigenschaften werden mit der Datei übertragen und nie synchronisiert oder verloren gehen. Wenn das Dateiformat das Speichern zusätzlicher Informationen unterstützt, empfiehlt es sich daher, die Eigenschaften in der Datei selbst zu speichern.

Der nächste Schritt besteht darin, zu bestimmen, welche Eigenschaften von der Datei bereitgestellt werden sollen. Vielleicht denken Sie anfänglich, dass ein eingeschränkter Satz von Eigenschaften ausreichend ist. Eine Audiodatei kann nur audiobezogene Eigenschaften unterstützen und dort enden. Bei dieser Audiodatei kann es sich jedoch um eine Aufzeichnung einer Gerichtssitzung handeln, die von einer Justiz Gesellschaft archiviert wurde. In diesem Fall möchte die Anwaltskanzlei sicherlich andere nicht-Audioeigenschaften dieser Datei zuordnen, wie z. b. die Fall Nummer. Der Anbieter des AudioDateiformats kann möglicherweise nicht alle Szenarien ermitteln, in denen das Format immer verwendet wird. Daher sollten Sie in Erwägung ziehen, die über das Eigenschaften System unterstützte beliebige Eigenschaft in einer beliebigen Eigenschaft zu aktivieren.

## <a name="legacy-technology"></a>Legacy Technologie

Die sekundäre Stream-Technologie von Microsoft Windows NT File System (NTFS) wurde entwickelt, um die Persistenz zusätzlicher Informationen mit der Datei über einen alternativen Stream zu unterstützen, der auf der Dateisystem Ebene festgelegt ist. Sie Fragen sich vielleicht, warum diese sekundären Datenströme nicht als Hauptmethode zum Speichern von Eigenschaften verwendet werden, insbesondere bei der Unterstützung offener Metadaten. Der Hauptgrund dafür ist die Übertragbarkeit dieser zusätzlichen Informationen. Leider werden diese alternativen Streams in vielen Szenarios entfernt, einschließlich Client seitiger Caching-Unterstützung (CSC), Senden von Dateien als Anlagen und Kopieren von Dateien in einen nicht-NTFS-Speicher.

Sekundäre Datenströme bieten keine robuste Lösung, in der die Eigenschaften sicher mit der Datei übertragen werden. Daher bietet das Windows Vista-Eigenschaften System keinen integrierten Mechanismus, mit dem die sekundären NTFS-Streams für den Eigenschaften Speicher ausgenutzt werden. Außerdem wird dringend davon abgeraten, Eigenschafts Handler zu entwickeln, die sekundäre Datenströme für die Speicherung von Eigenschaften verwenden. Natürlich gibt es Szenarios, in denen sekundäre NTFS-Datenströme geeignet sind. Dies gilt insbesondere dann, wenn Anwendungen sicherstellen können, dass die Datei, mit der Sie arbeiten, immer in einem NTFS-Volume gespeichert ist und nicht als Ergebnis der Interaktion von Endbenutzern verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaften Listen](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaften Handlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaften Handlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaften Handlern](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
