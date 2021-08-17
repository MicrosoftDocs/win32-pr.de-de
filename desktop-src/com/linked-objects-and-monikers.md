---
title: Verknüpfte Objekte und Moniker
description: Verknüpfte Objekte wie eingebettete Objekte basieren auf einem Objekthandler für die Kommunikation mit Serveranwendungen.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb8107a5c98ae407cc8e6198d782f75b092110232ae23f41a42dcaefae31758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736493"
---
# <a name="linked-objects-and-monikers"></a>Verknüpfte Objekte und Moniker

Verknüpfte Objekte wie eingebettete Objekte basieren auf einem Objekthandler für die Kommunikation mit Serveranwendungen. Das verknüpfte Objekt selbst verwaltet jedoch die Benennung und Nachverfolgung von Linkquellen. Das verknüpfte Objekt verhält sich wie ein Prozessserver. Wenn beispielsweise aktiviert, sucht ein verknüpftes Objekt die OLE-Serveranwendung, die die Linkquelle ist, und startet sie.

Der Handler eines verknüpften Objekts besteht aus zwei Hauptkomponenten: der Handlerkomponente und der Verknüpfungskomponente. Die Handlerkomponente enthält die Steuerungs- und Remotingteile und -funktionen ähnlich wie ein Handler für ein eingebettetes Objekt. Die Verknüpfungskomponente verfügt über einen eigenen Controller und Cache und bietet Zugriff auf den strukturierten Speicher des Objekts. Der Controller für verknüpfungskomponenten unterstützt die Quellbenennung durch die Verwendung von Monikern und die Bindung, den Prozess der Suche und Ausführung der Linkquelle. (Weitere Informationen zu Monikern und Bindungen finden Sie unter [The Component Object Model](the-component-object-model.md).)

Wenn ein Benutzer zunächst ein verknüpftes Objekt erstellt oder ein vorhandenes objekt aus dem Speicher lädt, lädt der Container eine Instanz der verknüpfenden Komponente zusammen mit dem Objekthandler in den Arbeitsspeicher. Die Verknüpfungskomponente stellt Schnittstellen bereit , insbesondere [**IOleLink,**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)die das Objekt als Link identifizieren und es ermöglichen, die Benennung, Nachverfolgung und Aktualisierung seiner Linkquelle zu verwalten.

Durch die Implementierung der [**IOleLink-Schnittstelle**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) stellt ein verknüpftes Objekt seinen Container mit Funktionen bereit, die das Verknüpfen unterstützen. Nur verknüpfte Objekte implementieren **IOleLink,** und durch Abfragen dieser Schnittstelle kann ein Container bestimmen, ob ein bestimmtes Objekt eingebettet oder verknüpft ist. Die wichtigste funktion, die von **IOleLink** bereitgestellt wird, ermöglicht es einem Container, eine Bindung an die Quelle des verknüpften Objekts zu erstellen, d. b. die Verbindung mit dem Dokument zu aktivieren, in dem die nativen Daten des verknüpften Objekts gespeichert sind. **IOleLink definiert** auch Funktionen zum Verwalten von Informationen über das verknüpfte Objekt, z. B. zwischengespeicherte Präsentationsdaten und den Speicherort der Linkquelle.

Wenn ein zusammengesetztes Dokument gespeichert wird, das ein verknüpftes Objekt enthält, werden die Daten des Links mit der Linkquelle und nicht mit dem Container gespeichert. Es werden nur Informationen zu Name und Speicherort zusammen mit dem Verbunddokument gespeichert. Dieses Verhalten steht im Gegensatz zu einem eingebetteten Objekt, dessen Daten zusammen mit dem des Containers gespeichert werden.

Containeranwendungen können Informationen zu ihren eingebetteten Objekten bereitstellen, damit letztere oder Teile davon als Linkquellen fungieren können. Durch die Implementierung von Unterstützung für das Verknüpfen mit eingebetteten Objekten Ihres Containers ermöglichen Sie geschachtelte Einbettungen, wodurch der Benutzer die Originale jedes Einbettungsobjekts nachverfolgen muss, zu dem ein Link gewünscht ist. Wenn ein Benutzer z. B. ein Microsoft Excel-Arbeitsblatt in Microsoft Word einbetten möchte und das Arbeitsblatt eine bitmap enthält, die in Paintbrush erstellt wurde, kann der Benutzer eine Verknüpfung mit einer Kopie der Bitmap im Arbeitsblatt anstelle des Originals erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbunddokumente](compound-documents.md)
</dt> <dt>

[In-Process-Server](in-process-servers.md)
</dt> <dt>

[Objekthandler](object-handlers.md)
</dt> </dl>

 

 




