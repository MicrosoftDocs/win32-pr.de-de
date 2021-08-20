---
title: Structured Storage Serialized Property Set Format
description: Persistente Eigenschaftensätze bieten eine Option zum Speichern von Daten in Dateisystementitäten. Es wird empfohlen, zum Erstellen und Verwalten die Schnittstellen IPropertySetStorage und IPropertyStorage zu verwenden, die unter Eigenschaften und Eigenschaftensätze beschrieben sind.
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- Structured Storage Strctd Stg , Grundlagen, serialisiertes Eigenschaftensatzformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acbc5300c04b4fe5a9b2a9ce2610eefc8608b3921ef52968a7165c4362ff7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959774"
---
# <a name="structured-storage-serialized-property-set-format"></a>Structured Storage Serialized Property Set Format

Persistente Eigenschaftensätze bieten eine Option zum Speichern von Daten in Dateisystementitäten. Es wird empfohlen, zum Erstellen und Verwalten die [**Schnittstellen IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) zu verwenden, die unter Eigenschaften und [Eigenschaftensätze beschrieben sind.](properties-and-property-sets.md)

Eigenschaftensätze bestehen aus einem markierten Abschnitt von Werten, bei dem der Abschnitt eindeutig durch einen Formatbezeichner (FMTID) identifiziert wird. Jede Eigenschaft besteht aus einem Eigenschaftenbezeichner und einem Typindikator, der einen Wert darstellt. Jeder in einem Eigenschaftensatz gespeicherte Wert verfügt über einen eindeutigen Eigenschaftenbezeichner, der die Eigenschaft unterscheidet. Der Typindikator beschreibt die Darstellung der Daten im Wert.

Wenn Sie die [**Schnittstellen IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) verwenden, müssen Sie die Formatstruktur für serialisierte COM-Eigenschaften nicht verarbeiten. Weitere Informationen finden Sie in den folgenden Themen:

Alle Datenelemente innerhalb eines Eigenschaftensets werden in intel-Darstellung (d. h. in Little-Endian-Byte-Reihenfolge) gespeichert.

COM definiert ein standardmäßiges serialisiertes Datenformat für Eigenschaftensätze. Bei der Verarbeitung des serialisierten Formats und nicht mit den Schnittstellen haben Eigenschaftensätze die folgenden Merkmale:

-   Eigenschaftensätze ermöglichen es verschiedenen Anwendungen, eigene unabhängige Eigenschaftensätze für die Anwendung zu erstellen.
-   Eigenschaftssätze können in einer einzelnen [**IStream-Instanz**](/windows/desktop/api/Objidl/nn-objidl-istream) oder in einer [**IStorage-Instanz**](/windows/desktop/api/Objidl/nn-objidl-istorage) gespeichert werden, die mehrere Streams enthält. Eigenschaftssätze sind einfach ein anderer Datentyp, der in vielen verschiedenen Formen eines In-Memory- oder On-Disk-Speichers gespeichert werden kann. Weitere Informationen und empfohlene Konventionen zum Erstellen des Zeichenfolgennamens für das Speicherobjekt finden Sie unter [Storage-Namenskonventionen.](storage-object-naming-conventions.md)
-   Eigenschaftensätze ermöglichen das Hinzufügen eines Wörterbuchs mit Anzeigenamen, die den Inhalt beschreiben. Es wird eine Reihe von Konventionen für die Auswahl von Eigenschaftsnamen empfohlen. Weitere Informationen zu diesem optionalen Wörterbuch finden Sie unter [Reserved Property Identifiers](reserved-property-identifiers.md), einschließlich [Eigenschaften-ID 0](/windows/desktop/Stg/reserved-property-identifiers).

Der Eigenschaftensatzstream ist in drei Hauptteile unterteilt:

-   Header
-   FORMATID-/Offsetpaar
-   Abschnitt mit den tatsächlichen Eigenschaftssatzwerten

Die Gesamtlänge des Eigenschaftensatzstreams muss kleiner oder gleich 256.000 sein. In den folgenden Abschnitten, [Property Set Header](property-set-header.md), Format [Identifier/Offset Pair](format-identifier-offset-pair.md)und [Section](section.md) (einschließlich [Eigenschaftenbezeichner/Offsetpaare)](property-identifiers-offset-pairs.md)mit unterstützenden Themen, werden die einzelnen Komponenten beschrieben, aus denen das Eigenschaftensatz-Datenformat erstellt wird.

> [!Note]  
> In früheren Versionen dieses Dokuments wurden Erweiterungen des Eigenschaftssatzstreams beschrieben, in denen mehr als ein Abschnitt zulässig ist. Dieser Abschnitt wurde jedoch überarbeitet, um einen Abschnitt im Eigenschaftenstream zur Verfügung zu stellen. Die einzige Ausnahme sind [Die DocumentSummaryInformation- und UserDefined-Eigenschaftensätze.](the-documentsummaryinformation-and-userdefined-property-sets.md)

 

 

 