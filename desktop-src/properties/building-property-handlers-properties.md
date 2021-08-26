---
description: Eigenschaften werden durch IDs dargestellt, die als Eigenschaftenbezeichner (PIDs) bekannt sind.
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Grundlegendes zu Eigenschaftenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42139a869551f0f4dc786f02c66c673a49495ba01f5258aeeff12051bd3f60b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946970"
---
# <a name="understanding-property-handlers"></a>Grundlegendes zu Eigenschaftenhandlern

Eigenschaften werden durch IDs dargestellt, die als Eigenschaftenbezeichner (PIDs) bekannt sind. Jede Eigenschaft MUSS über einen global eindeutigen Bezeichner (GLOBALLY UNIQUE IDENTIFIER, GUID) verfügen. Dieser Bezeichner besteht aus einer GUID, die eine Auflistung von Eigenschaften darstellt, die als Eigenschaftensatz bezeichnet werden, sowie entweder eine Zeichenfolge oder eine 32-Bit-Ganzzahl, um die Eigenschaft innerhalb des Sets zu identifizieren. Wenn die ganzzahlige Form der ID verwendet wird, werden die werte 0x00000000, 0xFFFFFFFF und 0xFFFFFFFE ungültig betrachtet. Anbieter können garantieren, dass ihre Eigenschaften eindeutig definiert sind, indem sie sie in einem Eigenschaftensatz platzieren, der durch ihre eigenen GUIDs definiert wird.

> [!IMPORTANT]
> Es ist wichtig, dass Sie Eigenschaften für die erste Version des Schemas sorgfältig und strategisch definieren. Alle Änderungen an benutzerdefinierten Eigenschaften (z. B. Spaltenbreite oder Eigenschaftentyp) werden in der Datenbank nicht berücksichtigt, nachdem ein Schema registriert wurde. Die einzige Möglichkeit, diese Änderungen zu erkennen, nachdem das Schema einmal auf einem System registriert wurde, besteht darin, den Index neu zu erstellen und dann das neue Schema zu registrieren oder das Schema zu registrieren und dann eine neue Eigenschaft (die aus einem kanonischen Namen und einem PKEY besteht) für jedes untergeordnete Release zu erstellen. z. B. `PKEY_GroupName_PropertyNameV2` `PKEY_GroupName_PropertyNameV3` , usw.). Wir raten davon ab, neue Eigenschaften auf diese Weise zu erstellen, da mehrere nicht sehr viele Spalten die Systemleistung beeinträchtigen können.

 

Dieses Thema ist wie folgt organisiert:

-   [Metadaten](#metadata)
    -   [Öffnen von Metadaten](#open-metadata)
-   [Informationen zu Eigenschaftenhandlern](#about-property-handlers)
-   [Legacytechnologie](#legacy-technology)
-   [Zugehörige Themen](#related-topics)

## <a name="metadata"></a>Metadaten

In Windows Vista und höher ist ein neues Eigenschaftensystem, das auf Metadaten basiert, von zentraler Bedeutung für die Organisation von Elementen wie Dateien, E-Mails und Kontakten. In diesem neuen Eigenschaftensystem können Elemente basierend auf ihren Metadaten durchsucht werden, und Benutzer können diese Metadaten lesen oder schreiben. Metadaten in diesem System werden durch einen erweiterbaren Satz von Eigenschaften dargestellt, *die* als Name-Wert-Paare implementiert werden.

In Windows Vista und höher deckt ein umfassender Satz von Eigenschaften die Besonderheiten von Elementen wie Fotos, Musik, Dokumenten, Nachrichten, Kontakten und Dateien ab. Unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) können ihre eigenen Eigenschaften auf der Plattform einführen, wenn keine vorhandene Eigenschaft ihre Anforderungen erfüllt.

### <a name="open-metadata"></a>Öffnen von Metadaten

Das Eigenschaftensystem in Windows Vista und höher ist ein offenes Metadatensystem. Ein Dateiformat speichert jede zugewiesene Eigenschaft und macht diesen Wert bei der Abfrage verfügbar, unabhängig von Relevanz oder Bedeutung. Dadurch können Entwickler von Drittanbietern zusätzliche Eigenschaften an die Datei anfügen, ohne dass der zugeordnete Eigenschaftenhandler geändert werden muss. Open Metadata ist ein leistungsstarkes Konzept. Weitere Informationen zur Unterstützung von offenen Metadaten für ein XML-basiertes Dateiformat finden Sie unter "Supporting Open Metadata" (Unterstützen von offenen Metadaten) in [Initializing Property Handlers (Initialisieren von Eigenschaftenhandlern).](./building-property-handlers-property-handlers.md)

> [!Note]  
> Eigenschaftenhandler sind immer bestimmten Dateitypen zugeordnet. Wenn Ihr Dateiformat Eigenschaften enthält, die einen benutzerdefinierten Eigenschaftenhandler erfordern, sollten Sie daher immer eine eindeutige Dateierweiterung für jedes Dateiformat registrieren.

 

## <a name="about-property-handlers"></a>Informationen zu Eigenschaftenhandlern

In Windows Vista und höher verfügt Windows über ein erweiterbares Eigenschaftensystem zum Speichern und Abrufen von Metadaten in den Dateien und Datenelementen, auf die Sie zugreifen. Windows Explorer und das Windows Search-System verwenden zusammen mit anderen Anwendungen Eigenschaftenhandler, um diese Metadaten zu lesen und zu ändern. Wenn Sie ein Entwickler sind, der einen bestimmten Dateityp besitzt, sollten Sie einen Eigenschaftenhandler registrieren, um dem Eigenschaftensystem Zugriff auf die Metadaten in Ihren Dateien zu geben. In einigen Fällen können Sie möglicherweise einen vorhandenen Eigenschaftenhandler verwenden, der Ihr Dateiformat und seine Eigenschaften lesen und verstehen kann. In anderen Fällen müssen Sie möglicherweise einen neuen Eigenschaftenhandler für Ihren Dateityp entwickeln.

Der erste Schritt beim Schreiben eines Eigenschaftenhandlers besteht in der Berücksichtigung der Eigenschaften, die ihr Dateityp unterstützt. Eigenschaftswerte werden im Dateistream gespeichert, in erster Linie, um die Transportierbarkeit zu ermöglichen. Wenn die Eigenschaftswerte wie in diesem System in der Datei selbst gespeichert werden, kann ein Benutzer eine Datei auf einen anderen Computer, ein USB-Speicherlaufwerk oder ein anderes Dateisystem kopieren oder die Datei als E-Mail-Anlage senden. Die Eigenschaften werden mit der Datei übertragen und werden nie synchronisiert oder verloren. Wenn das Dateiformat das Speichern zusätzlicher Informationen unterstützt, ist es daher am besten, die Eigenschaften in der Datei selbst zu speichern.

Im nächsten Schritt wird bestimmt, welche Eigenschaften die Datei bereitstellen soll. Sie könnten zunächst der Meinung sein, dass ein begrenzter Satz von Eigenschaften angemessen ist. Eine Audiodatei kann nur audiobezogene Eigenschaften unterstützen und dort enden. Bei dieser Audiodatei kann es sich jedoch um eine Aufzeichnung einer Sitzung eines Von einer Rechtshedynten archivierten Rechtshedings oder einer Rechtskauedungseinheit (Law Firm, NSD) auszeichnen. In diesem Fall möchte die Sotline dieser Datei sicherlich andere Nicht-Audioeigenschaften zuordnen, z. B. die Fallnummer. Der Anbieter des Audiodateiformats kann möglicherweise nicht alle Szenarien bestimmen, in denen sein Format jemals verwendet wird. Daher sollten sie erwägen, die speicherung beliebiger Eigenschaften zu aktivieren, die vom Eigenschaftensystem unterstützt werden.

## <a name="legacy-technology"></a>Legacytechnologie

Microsoft Windows SEKUNDÄRE STREAM-Technologie (NT File System, NTFS) wurde entwickelt, um die Persistenz zusätzlicher Informationen mit der Datei über einen alternativen Stream zu unterstützen, der auf Dateisystemebene festgelegt ist. Vielleicht fragen Sie sich, warum diese sekundären Datenströme nicht als Hauptmethode zum Speichern von Eigenschaften verwendet werden, insbesondere bei unterstützung offener Metadaten. Der Hauptgrund ist die Transportierbarkeit dieser zusätzlichen Informationen. Leider werden diese alternativen Streams in vielen Szenarien entfernt, einschließlich clientseitiger Cacheunterstützung (Client-Side Caching Support, CSC), Senden von Dateien als Anlagen und Kopieren von Dateien in einen Nicht-NTFS-Speicher.

Sekundäre Streams bieten keine stabile Lösung, bei der Eigenschaften garantiert mit der Datei übermittelt werden. Daher bietet das Windows Vista-Eigenschaftensystem keinen integrierten Mechanismus, der die sekundären NTFS-Datenströme für den Eigenschaftenspeicher ausnutzt. ISVs wird auch dringend davon abgeraten, Eigenschaftenhandler zu erstellen, die sekundäre Streams für die Speicherung von Eigenschaften verwenden. Natürlich gibt es Szenarien, in denen sekundäre NTFS-Streams geeignet sind, insbesondere dann, wenn Anwendungen garantieren können, dass die Datei, mit der sie es zu tun haben, immer auf einem NTFS-Volume gespeichert ist und nicht als Folge der Interaktion des Endbenutzers verschoben wird.

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

 

 
