---
description: Eigenschaften werden durch IDs dargestellt, die als Eigenschaftsbezeichner (PIDs) bezeichnet werden.
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Grundlegendes zu Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b44d0a3a6d0a1b6c929eb151551155d0b5435a0
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481935"
---
# <a name="understanding-property-handlers"></a>Grundlegendes zu Eigenschaftenhandlern

Eigenschaften werden durch IDs dargestellt, die als Eigenschaftsbezeichner (PIDs) bezeichnet werden. Jede Eigenschaft MUSS einen global eindeutigen Bezeichner (GLOBALLYD) aufweisen. Dieser Bezeichner besteht aus einer GUID, die eine Auflistung von Eigenschaften darstellt, die als Eigenschaftensatz bezeichnet werden, sowie eine Zeichenfolge oder eine 32-Bit-Ganzzahl, um die Eigenschaft innerhalb des Satzes zu identifizieren. Wenn die ganzzahlige Form der ID verwendet wird, werden die Werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE als ungültig betrachtet. Anbieter können sicherstellen, dass ihre Eigenschaften eindeutig definiert werden, indem sie sie in einem Eigenschaftensatz platzieren, der durch ihre eigenen GUIDs definiert wird.

> [!IMPORTANT]
> Es ist wichtig, dass Sie Eigenschaften für die erste Version des Schemas sorgfältig und strategisch definieren. Änderungen an benutzerdefinierten Eigenschaften (z. B. Spaltenbreite oder Eigenschaftstyp) werden in der Datenbank nicht wiedergegeben, nachdem ein Schema registriert wurde. Die einzige Möglichkeit, diese Änderungen zu erkennen, nachdem das Schema einmal auf einem System registriert wurde, besteht darin, entweder den Index neu zu erstellen und dann das neue Schema zu registrieren oder das Schema zu registrieren und dann eine neue Eigenschaft (die aus einem kanonischen Namen und einem PKEY besteht) für jedes untergeordnete Release zu erstellen. z. `PKEY_GroupName_PropertyNameV2` B. `PKEY_GroupName_PropertyNameV3` , usw.). Es wird nicht empfohlen, auf diese Weise neue Eigenschaften zu erstellen, da sich mehrere überflüssige Spalten auf die Systemleistung auswirken können.

 

Dieses Thema ist wie folgt organisiert:

-   [Metadaten](#metadata)
    -   [Öffnen von Metadaten](#open-metadata)
-   [Informationen zu Eigenschaftenhandlern](#about-property-handlers)
-   [Legacytechnologie](#legacy-technology)
-   [Verwandte Themen](#related-topics)

## <a name="metadata"></a>Metadaten

In Windows Vista und höher ist ein neues Eigenschaftensystem, das auf Metadaten basiert, von zentraler Bedeutung für die Organisation von Elementen wie Dateien, E-Mails und Kontakten. In diesem neuen Eigenschaftensystem können Elemente basierend auf ihren Metadaten durchsucht werden, und Benutzer können diese Metadaten lesen oder schreiben. Metadaten in diesem System werden durch einen erweiterbaren Satz von *Eigenschaften* dargestellt, die als Name-Wert-Paare implementiert werden.

In Windows Vista und höher deckt ein umfassender Satz von Eigenschaften die Besonderheiten von Elementen wie Fotos, Musik, Dokumenten, Nachrichten, Kontakten und Dateien ab. Unabhängige Softwarehersteller (Independent Software Vendors, ISVs) können ihre eigenen Eigenschaften auf der Plattform einführen, wenn keine vorhandene Eigenschaft ihren Anforderungen entspricht.

### <a name="open-metadata"></a>Öffnen von Metadaten

Das Eigenschaftensystem in Windows Vista und höher ist ein offenes Metadatensystem. Ein Dateiformat speichert jede zugewiesene Eigenschaft und macht diesen Wert beim Abfragen verfügbar, unabhängig von Relevanz oder Bedeutung. Dadurch können Drittanbieterentwickler zusätzliche Eigenschaften an die Datei anfügen, ohne dass eine Änderung des zugeordneten Eigenschaftenhandlers erforderlich ist. Offene Metadaten sind ein leistungsstarkes Konzept. Weitere Informationen zur Unterstützung von offenen Metadaten für ein XML-basiertes Dateiformat finden Sie unter "Supporting Open Metadata" (Unterstützen von offenen Metadaten) unter [Initializing Property Handlers (Initialisieren von Eigenschaftenhandlern).](./building-property-handlers-property-handlers.md)

> [!Note]  
> Eigenschaftenhandler sind immer bestimmten Dateitypen zugeordnet. Wenn Ihr Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaftenhandler erfordern, sollten Sie daher immer eine eindeutige Dateinamenerweiterung für jedes Dateiformat registrieren.

 

## <a name="about-property-handlers"></a>Informationen zu Eigenschaftenhandlern

In Windows Vista und höher verfügt Windows über ein erweiterbares Eigenschaftensystem zum Speichern und Abrufen von Metadaten in den Dateien und Datenelementen, auf die Sie zugreifen. Windows Explorer und das Windows Search-System verwenden zusammen mit anderen Anwendungen Eigenschaftenhandler, um diese Metadaten zu lesen und zu ändern. Wenn Sie ein Entwickler sind, der einen bestimmten Dateityp besitzt, sollten Sie einen Eigenschaftenhandler registrieren, um dem Eigenschaftensystem Zugriff auf die Metadaten in Ihren Dateien zu gewähren. In einigen Fällen können Sie möglicherweise einen vorhandenen Eigenschaftenhandler verwenden, der Ihr Dateiformat und seine Eigenschaften lesen und verstehen kann. In anderen Fällen müssen Sie möglicherweise einen neuen Eigenschaftenhandler für Ihren Dateityp entwickeln.

Der erste Schritt beim Schreiben eines Eigenschaftenhandlers besteht darin, zu berücksichtigen, welche Eigenschaften Ihr Dateityp unterstützt. Eigenschaftswerte werden im Dateistream gespeichert, in erster Linie, um transportability zu ermöglichen. Wenn die Eigenschaftswerte wie in diesem System in der Datei selbst gespeichert werden, kann ein Benutzer eine Datei auf einen anderen Computer, einen USB-Speicherstick oder ein anderes Dateisystem kopieren oder die Datei als E-Mail-Anlage senden. Die Eigenschaften werden mit der Datei übertragen und werden nie nicht mehr synchronisiert oder verloren gehen. Wenn das Dateiformat das Speichern zusätzlicher Informationen unterstützt, ist es daher am besten, die Eigenschaften in der Datei selbst zu speichern.

Im nächsten Schritt wird bestimmt, welche Eigenschaften die Datei bereitstellen soll. Sie könnten anfangs denken, dass ein begrenzter Satz von Eigenschaften angemessen ist. Eine Audiodatei könnte nur audiobezogene Eigenschaften unterstützen und dort enden. Bei dieser Audiodatei kann es sich jedoch um eine Aufzeichnung einer Von einer Anwaltskanzlei archivierten Sitzung eines Schwiegers entscheiden. In diesem Fall möchte die Anwaltskanzlei dieser Datei sicherlich andere Nicht-Audioeigenschaften zuordnen, z. B. die Fallnummer. Der Anbieter des Audiodateiformats kann möglicherweise nicht alle Szenarien bestimmen, in denen ihr Format jemals verwendet wird. Daher sollten sie erwägen, die speicherung beliebiger Eigenschaften zu ermöglichen, die vom Eigenschaftensystem unterstützt werden.

## <a name="legacy-technology"></a>Legacytechnologie

Die sekundäre Streamtechnologie von Microsoft Windows NT File System (NTFS) wurde entwickelt, um die Persistenz zusätzlicher Informationen mit der Datei über einen alternativen Streamsatz auf Dateisystemebene zu unterstützen. Man könnte sich fragen, warum diese sekundären Datenströme nicht als Hauptmethode zum Speichern von Eigenschaften verwendet werden, insbesondere bei der Unterstützung von offenen Metadaten. Der Hauptgrund ist die Transportierbarkeit dieser zusätzlichen Informationen. Leider werden diese alternativen Streams in vielen Szenarien entfernt, z. B. unterstützung für clientseitiges Zwischenspeichern (Client-Side Caching Support, CSC), Senden von Dateien als Anlagen und Kopieren von Dateien in einen Nicht-NTFS-Speicher.

Sekundäre Streams bieten keine stabile Lösung, bei der Eigenschaften garantiert mit der Datei übertragen werden. Daher bietet das Windows Vista-Eigenschaftensystem keinen integrierten Mechanismus, der die sekundären NTFS-Datenströme für den Eigenschaftenspeicher nutzt. ISVs wird außerdem dringend davon abgeraten, Eigenschaftenhandler zu erstellen, die sekundäre Datenströme zum Speichern von Eigenschaften verwenden. Natürlich gibt es Szenarien, in denen sekundäre NTFS-Datenströme geeignet sind, insbesondere wenn Anwendungen garantieren können, dass die Datei, mit der sie zu tun haben, immer in einem NTFS-Volume gespeichert wird und aufgrund der Endbenutzerinteraktion nicht unterwegs ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Kind-Namen](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Verwenden von Eigenschaftenlisten](./building-property-handlers-property-lists.md)
</dt> <dt>

[Initialisieren von Eigenschaftenhandlern](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrieren und Verteilen von Eigenschaftenhandlern](./prophand-reg-dist.md)
</dt> <dt>

[Bewährte Methoden und häufig gestellte Fragen zu Eigenschaftenhandlern](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
