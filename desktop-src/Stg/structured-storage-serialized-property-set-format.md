---
title: Serialisiertes Eigenschaften Satz Format für strukturierte Speicherung
description: Persistente Eigenschaften Sätze stellen eine Option zum Speichern von Daten in Dateisystem Entitäten bereit. Es wird empfohlen, Sie zu erstellen und zu verwalten, indem Sie die IPropertySetStorage-Schnittstelle und die IPropertyStorage-Schnittstelle verwenden, die unter Eigenschaften und Eigenschaften Sätze beschrieben werden.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Strukturierter Speicherplatz Halter-STG, Grundlagen, serialisiertes Eigenschaften Satz Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea03d5ccab337897be801840080e83a6fa86880
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340722"
---
# <a name="structured-storage-serialized-property-set-format"></a>Serialisiertes Eigenschaften Satz Format für strukturierte Speicherung

Persistente Eigenschaften Sätze stellen eine Option zum Speichern von Daten in Dateisystem Entitäten bereit. Es wird empfohlen, Sie zu erstellen und zu verwalten, indem Sie die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle und die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle verwenden, die unter [Eigenschaften und Eigenschaften Sätze](properties-and-property-sets.md)beschrieben werden.

Eigenschafts Sätze bestehen aus einem markierten Abschnitt von Werten, wobei der Abschnitt eindeutig durch einen Format Bezeichner (fmtid) identifiziert wird. Jede Eigenschaft besteht aus einem Eigenschaften Bezeichner und einem Typindikator, der einen Wert darstellt. Jeder in einem Eigenschaften Satz gespeicherte Wert verfügt über einen eindeutigen Eigenschaften Bezeichner, der die Eigenschaft unterscheidet. Der Typindikator beschreibt die Darstellung der Daten im-Wert.

Wenn Sie die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle und die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle verwenden, müssen Sie die Format Struktur der serialisierten com-Eigenschaften Menge nicht verarbeiten. Weitere Informationen finden Sie in den aufgelisteten Themen:

Alle Datenelemente in einem Eigenschaften Satz werden in der Intel-Darstellung gespeichert (d. h. in Little-Endian-Byte Reihenfolge).

COM definiert ein serialisiertes Standarddatenformat für Eigenschaften Sätze. Wenn das serialisierte Format und nicht die Schnittstellen verarbeitet werden, haben Eigenschafts Sätze die folgenden Eigenschaften:

-   Mit Eigenschafts Sätzen können unterschiedliche Anwendungen ihre eigenen unabhängigen Eigenschaften Sätze erstellen, die für die Anwendung bereitgestellt werden.
-   Eigenschaften Sätze können in einer einzelnen [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Instanz oder in einer [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Instanz gespeichert werden, die mehrere Datenströme enthält. Eigenschaften Sätze sind einfach ein anderer Datentyp, der in vielen verschiedenen Formen eines Speicher internen oder Speicher internen Speichers gespeichert werden kann. Weitere Informationen und empfohlene Konventionen zum Erstellen des Zeichen folgen namens für das Speicher Objekt finden Sie unter [Benennungs Konventionen für Speicher Objekte](storage-object-naming-conventions.md).
-   Mit Eigenschafts Sätzen kann ein Wörterbuch mit anzeigen Amen eingeschlossen werden, die den Inhalt beschreiben. Eine Reihe von Konventionen für die Auswahl von Eigenschaften Namen wird empfohlen. Weitere Informationen zu diesem optionalen Wörterbuch finden Sie unter [reservierte Eigenschaften](reserved-property-identifiers.md)Bezeichner, einschließlich der Eigen [schafts-ID 0](/windows/desktop/Stg/reserved-property-identifiers).

Der Eigenschafts Satz-Stream ist in drei Hauptbestandteile unterteilt:

-   Header
-   FormatID/Offset-paar
-   Abschnitt, der die tatsächlichen Eigenschaften Satz Werte enthält

Die Gesamtlänge des Eigenschaften Satz-Streams muss kleiner oder gleich 256 KB sein. Die folgenden Abschnitte, die [Eigenschaften Satz Kopfzeile](property-set-header.md), das [Format-ID/Offset-paar](format-identifier-offset-pair.md)und den [Abschnitt](section.md) (einschließlich der Eigenschaften Bezeichner [/Offset-Paare](property-identifiers-offset-pairs.md)) mit unterstützenden Themen beschreiben die einzelnen Komponenten, die das Eigenschafts Satz-Daten Format bilden.

> [!Note]  
> In früheren Versionen dieses Dokuments wurden Erweiterungen zum Eigenschaften Satz-Stream mit mehr als einem zulässigen Abschnitt beschrieben, aber das wurde überarbeitet, um einen Abschnitt im Eigenschaftenstream bereitzustellen. Die einzige Ausnahme sind [die documentsummaryinformation-und UserDefined-Eigenschaften Sätze](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

 

 