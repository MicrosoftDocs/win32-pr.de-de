---
description: Eigenschaften, die im Eigenschaften System von Windows Vista und höher verwendet werden, werden in Eigenschafts Schemas deklariert.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Erstellen von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346648"
---
# <a name="creating-custom-properties"></a>Erstellen von benutzerdefinierten Eigenschaften

Eigenschaften, die im Eigenschaften System von Windows Vista und höher verwendet werden, werden in Eigenschafts Schemas deklariert. Diese Eigenschafts Schemas werden in XML-Dateien definiert und beschreiben verschiedene Aspekte einer Eigenschaft, einschließlich ihres Typs (einschließlich der Informationen über den primitiven Typ und die mehrwertige Angabe), wie Sie in der Windows-Benutzeroberfläche angezeigt werden können, welche Art von Bezeichnungen (benutzerfreundliche Bearbeitungs Zeichenfolgen) verwendet werden sollen und wie Sie im Such Speicher zwischengespeichert werden, um schnelleren Zugriff zu erhalten. Eigenschaften werden anhand ihres kanonischen Namens oder Ihres Eigenschafts Schlüssels (pkey) identifiziert.

Ein kanonischer Name ist der leserfreundliche Name der Eigenschaft und verwendet eine Namespace Konvention ähnlich der in Microsoft .net. Für System definierte Eigenschaften (in Windows enthaltene Eigenschaften) ist die Konvention `System.GroupName.PropertyName` . Beachten Sie, dass das Pascal-Schreib Schema, in dem Buchstaben am Anfang jedes Worts groß geschrieben werden, in diesen Namen verwendet wird. Kanonische Namen werden an verschiedenen Stellen verwendet, einschließlich der Eigenschaften Listen und Spaltennamen im Eigenschaften Cache. Sie werden daher in Structured Query Language (SQL)-Abfragen verwendet, um einen Eigenschafts Wert abzurufen.

Ein pkey ist ein Wertepaar, das aus einer GUID und einem **DWORD** besteht, die als *FormatID* bzw. *PROPID* bezeichnet werden. Sie wird durch eine [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) -Struktur dargestellt. Die meisten der Eigenschaften System-APIs akzeptieren diese Eigenschafts Schlüssel. Das Windows Software Development Kit (SDK) enthält die Header Datei propkey. h, die eine Makro Definition der einzelnen `System` Eigenschafts Schlüssel mit der Konvention von enthält `PKEY_GroupName_PropertyName` . Beispielsweise `PKEY_Photo_DateTaken` ist der Eigenschafts Schlüssel für die Eigenschaft mit dem kanonischen Namen `System.Photo.DateTaken` . Eigenschaftswerte werden in Form einer [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur gespeichert, bei der es sich um eine Erweiterung der OLE VARIANT-Typen handelt.

Dieser Abschnitt enthält das folgende Thema, das für das Erstellen von benutzerdefinierten Eigenschaften ganzzahlig ist:

-   [Grundlegendes zum Eigenschafts Beschreibungs Schema](./propdesc-schema-entry.md)

> [!Note]  
> Aufgrund möglicher Schwierigkeiten, die der Indexer bei der Verwendung des Schema Schema des Eigenschaften Systems aufweisen kann, ist es wichtig, Attribute sorgfältig und strategisch für die erste Version des Schemas zu definieren. Alle Änderungen an Attributen (Typ, Spaltenbreite, ggf.) werden in der Datenbank nach der Registrierung eines Schemas nicht wiedergegeben. Die einzigen Möglichkeiten, diese Änderungen zu erkennen, nachdem das Schema einmal auf einem System registriert wurde, würden entweder den Index neu erstellen und dann das neue Schema registrieren oder das Schema registrieren und dann für jede nachfolgende Version eine neue Eigenschaft erstellen. beispielsweise `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` usw.). Es wird nicht empfohlen, neue Eigenschaften auf diese Weise zu erstellen, da sich mehrere überflüssige Spalten möglicherweise auf die Systemleistung auswirken.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren von Eigenschaften Handlern](./building-property-handlers.md)
</dt> <dt>

[Eigenschafts Beschreibungs Schema](./propdesc-schema-entry.md)
</dt> </dl>

 

 
