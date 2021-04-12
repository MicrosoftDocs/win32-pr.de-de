---
title: Verknüpfte Objekte und Moniker
description: Verknüpfte Objekte, wie eingebettete Objekte, verlassen sich auf einen Objekt Handler, um mit Server Anwendungen zu kommunizieren.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207265"
---
# <a name="linked-objects-and-monikers"></a>Verknüpfte Objekte und Moniker

Verknüpfte Objekte, wie eingebettete Objekte, verlassen sich auf einen Objekt Handler, um mit Server Anwendungen zu kommunizieren. Das verknüpfte Objekt selbst verwaltet jedoch die Benennung und Nachverfolgung von Verknüpfungs Quellen. Das verknüpfte Objekt verhält sich wie ein Prozess interner Server. Wenn beispielsweise ein verknüpftes Objekt aktiviert ist, wird die OLE-Serveranwendung, die die Verknüpfungs Quelle ist, gesucht und gestartet.

Der Handler eines verknüpften Objekts besteht aus zwei Hauptkomponenten: der Handlerkomponente und der Verknüpfungs Komponente. Die Handlerkomponente enthält die Steuerungs-und Remoting-Teile und-Funktionen, ähnlich wie ein Handler für ein eingebettetes Objekt. Die Verknüpfungs Komponente verfügt über einen eigenen Controller und Cache und ermöglicht den Zugriff auf den strukturierten Speicher des Objekts. Der Verknüpfungs Komponenten Controller unterstützt die Quell Benennung durch die Verwendung von Monikern und die Bindung, das Auffinden und Ausführen der Link Quelle. (Weitere Informationen zu Monikern und Bindung finden Sie [im Component Object Model](the-component-object-model.md).)

Wenn ein Benutzer anfänglich ein verknüpftes Objekt erstellt oder ein vorhandenes Objekt aus dem Speicher lädt, lädt der Container zusammen mit dem Objekt Handler eine Instanz der Verknüpfungs Komponente in den Arbeitsspeicher. Die Verknüpfungs Komponente stellt Schnittstellen – insbesondere [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)– bereit, die das Objekt als Link bezeichnen und es Ihnen ermöglichen, die Benennung, Nachverfolgung und Aktualisierung der zugehörigen Verknüpfungs Quelle zu verwalten.

Durch Implementieren der [**iolelink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) -Schnittstelle stellt ein verknüpftes Objekt seinen Container mit Funktionen bereit, die das Verknüpfen unterstützen. **Iolelink** wird nur von verknüpften Objekten implementiert, und durch Abfragen für diese Schnittstelle kann ein Container ermitteln, ob ein bestimmtes Objekt eingebettet oder verknüpft ist. Die wichtigste Funktion von **iolelink** ermöglicht einem Container das Binden an die Quelle des verknüpften Objekts, d. h., um die Verbindung mit dem Dokument zu aktivieren, in dem die systemeigenen Daten des verknüpften Objekts gespeichert werden. **Iolelink** definiert auch Funktionen zum Verwalten von Informationen über das verknüpfte Objekt, z. b. zwischengespeicherte Präsentationsdaten und den Speicherort der Verknüpfungs Quelle.

Wenn ein Verbund Dokument gespeichert wird, das ein verknüpftes Objekt enthält, werden die Daten des Links mit der Link Quelle, nicht mit dem Container gespeichert. Nur Informationen zu Name und Speicherort werden zusammen mit dem Verbund Dokument gespeichert. Dieses Verhalten steht im Gegensatz zu dem eines eingebetteten Objekts, dessen Daten zusammen mit dem des zugehörigen Containers gespeichert werden.

Container Anwendungen können Informationen zu ihren eingebetteten Objekten bereitstellen, sodass die letzteren oder Teile davon als Verknüpfungs Quellen fungieren können. Durch Implementieren der Unterstützung für das Verknüpfen mit den eingebetteten Objekten des Containers können Sie geschiebte Einbettungen ermöglichen, sodass der Benutzer die Originale der einzelnen Einbettungs Objekte, auf die ein Link gewünscht ist, nicht mehr nachverfolgen muss. Wenn ein Benutzer beispielsweise ein Microsoft Excel-Arbeitsblatt in Microsoft Word einbetten möchte und das Arbeitsblatt eine in Pinsel erstellte Bitmap enthält, kann der Benutzer eine Verknüpfung mit einer Kopie der Bitmap herstellen, die im Arbeitsblatt enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbund Dokumente](compound-documents.md)
</dt> <dt>

[Prozess interne Server](in-process-servers.md)
</dt> <dt>

[Objekt Handler](object-handlers.md)
</dt> </dl>

 

 




