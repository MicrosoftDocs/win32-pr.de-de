---
title: Eigenschaften und Eigenschaftensätze
description: Die Arten von Laufzeiteigenschaften, die Von Automation und Microsoft ActiveX Controls angeboten werden, sind zwar wichtig, aber sie stellen nicht direkt die Notwendigkeit dar, Informationen mit Objekten zu speichern, die dauerhaft im Dateisystem gespeichert sind.
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- Strukturierte Storage Strctd Stg, Grundlagen, Eigenschaften und Eigenschaftensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df2ef4b3e4d91cc908d82b58a0ec0156a60de23208cfd8dde2718fa62eaab60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662260"
---
# <a name="properties-and-property-sets"></a>Eigenschaften und Eigenschaftensätze

Die Arten von Laufzeiteigenschaften, die Von Automation und Microsoft ActiveX Controls angeboten werden, sind zwar wichtig, aber sie stellen nicht direkt die Notwendigkeit dar, Informationen mit Objekten zu speichern, die dauerhaft im Dateisystem gespeichert sind. Diese Entitäten können Dateien (strukturiert, zusammengesetzt usw.), Verzeichnisse und Zusammenfassungskataloge enthalten. COM bietet sowohl ein serialisiertes Standardformat für diese persistenten Eigenschaften als auch eine Reihe von Schnittstellen und Funktionen, mit denen Sie die Eigenschaftensätze und deren Eigenschaften erstellen und bearbeiten können.

Persistente Eigenschaften werden als Sätze gespeichert, und einer Dateisystementität können eine oder mehrere Sätze zugeordnet werden. Diese persistenten Eigenschaftensätze sollen zum Speichern von Daten verwendet werden, die als Sammlung von fein abgrenzenden Werten dargestellt werden können. Sie sind nicht für die Verwendung als große Datenbank vorgesehen. Sie können verwendet werden, um Zusammenfassende Informationen zu einem Objekt im System zu speichern, auf das dann von jedem anderen Objekt zugegriffen werden kann, das versteht, wie dieser Eigenschaftensatz interpretiert werden soll.

Frühere Versionen von COM haben in Bezug auf Eigenschaften und deren Verwendung nur sehr wenig angegeben, aber es wurde ein serialisiertes Format definiert, mit dem Entwickler Eigenschaften und Eigenschaftensätze in einer [**IStorage-Instanz speichern**](/windows/desktop/api/Objidl/nn-objidl-istorage) konnten. Die Eigenschaftenbezeichner und die Semantik eines einzelnen Eigenschaftensets, die für zusammenfassende Informationen zu einem Dokument verwendet werden, wurden ebenfalls definiert. Zu diesem Zeitpunkt war es erforderlich, diese Struktur direkt als Datenstrom zu erstellen und zu bearbeiten. Siehe [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

Com definiert nun jedoch zwei primäre Schnittstellen zum Verwalten von Eigenschaftensätzen:

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

Es ist nicht mehr erforderlich, das serialisierte Format direkt zu behandeln, wenn diese Schnittstellen für ein Objekt implementiert werden, das die [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) unterstützt (z. B. Verbunddateien). Beim Schreiben von Eigenschaften über [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) werden Daten erstellt, die genau dem COM-Eigenschaftensatzformat entsprechen, wie es über **IStorage-Methoden angezeigt** wird. Umgekehrt gilt auch : Eigenschaften, die mithilfe von **IStorage** in das COM-Eigenschaftensatzformat geschrieben werden, sind über **IPropertySetStorage** und **IPropertyStorage** sichtbar (obwohl Sie nicht erwarten können, in [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) zu schreiben, und die Eigenschaften über **IPropertyStorage** sofort verfügbar sind oder umgekehrt).

Die [**IPropertySetStorage-Schnittstelle definiert**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Methoden, die Eigenschaftensätze erstellen und verwalten. Die [**IPropertyStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) bearbeitet die Eigenschaften innerhalb eines Eigenschaftensets direkt. Durch Aufrufen der Methoden dieser Schnittstellen kann ein Anwendungsentwickler alle Eigenschaftensätze verwalten, die für eine bestimmte Dateisystementität geeignet sind. Die Verwendung dieser Schnittstellen bietet eine optimierten Lese- und Schreibimplementierung für Eigenschaften, anstatt in jeder Anwendung eine Implementierung zu haben, bei der Leistungsengpässe wie z. B. eine unaufdingliche Suche möglich sind. Sie können die Schnittstellen implementieren, um die Leistung zu verbessern, sodass Eigenschaften schneller gelesen und geschrieben werden können, z. B. durch effizienteres Zwischenspeichern. Darüber hinaus ermöglichen **IPropertyStorage** und **IPropertySetStorage** das Bearbeiten von Eigenschaften für Entitäten, die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)nicht unterstützen, obwohl dies in der Regel von den meisten Anwendungen nicht unterstützt wird.

Dieser Abschnitt enthält die folgenden Themen:

-   [Der Eigenschaftssatz "Zusammenfassungsinformationen"](the-summary-information-property-set.md)
-   [Vordefinierte Formatbezeichner für Eigenschaftensatz](predefined-property-set-format-identifiers.md)
-   [Die Eigenschaftensätze DocumentSummaryInformation und UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementierungen von Eigenschaftensatz in COM](property-set-implementations-in-com.md)
</dt> <dt>

[Überlegungen zum Eigenschaftensatz](property-set-considerations.md)
</dt> <dt>

[Verwalten von Eigenschaften](managing-properties.md)
</dt> <dt>

[Verwalten von Eigenschaftensätzen](managing-property-sets.md)
</dt> <dt>

[Speichern von Eigenschaftensätzen](storing-property-sets.md)
</dt> <dt>

[Leistungsmerkmale](performance-characteristics.md)
</dt> </dl>

 

 




