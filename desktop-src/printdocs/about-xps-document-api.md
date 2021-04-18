---
description: Die XPS-Dokument-API implementiert das XPS-Objektmodell und ermöglicht Entwicklern das Erstellen eines XPS-OM, das Bearbeiten von XPS-Dokument Inhalten in systemeigenen Windows \\ \\ -Programmen und das Speichern des XPS-Maps in einer Datei oder einem Stream als XPS-Dokument.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informationen zur XPS-Dokument-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351010"
---
# <a name="about-xps-document-api"></a>Informationen zur XPS-Dokument-API

Die [XPS-Dokument-API](documents-xps.md) implementiert das XPS-Objektmodell und ermöglicht Entwicklern das Erstellen eines XPS-OM, das Bearbeiten von XPS-Dokument Inhalten in systemeigenen Windows \\ \\ -Programmen und das Speichern des XPS-Maps in einer Datei oder einem Stream als XPS-Dokument. Entwickler von XPSDrv-Filter Pipeline Modulen können auch die XPS-Dokument-API verwenden, um XPS-Dokumentinhalte in einem XPSDrv-Druckertreiber Filter zu bearbeiten.

## <a name="xps-document-api-overview"></a>Übersicht über XPS-Dokument-API

Das XPS-Objektmodell ist das Informationsmodell eines XPS-Dokuments. Das Informationsmodell des XPS-Dokuments ist von dem Markup Modell getrennt, das in den Dokument Teilen verwendet wird. Das XPS-Objektmodell beschreibt die Organisation der internen Komponenten, aus denen ein XPS-Dokument besteht, und das Markup Modell beschreibt den Inhalt dieser Komponenten.

In einem Programm wird das XPS-Objektmodell als XPS-OM instanziiert. Beim XPS-OM handelt es sich im Wesentlichen um eine in-Memory-Version des Inhalts eines XPS-Dokuments. Obwohl es in der logischen Organisation zu einem XPS-Dokument kommt, wird ein XPS-OM-Objekt erst als XPS-Dokument betrachtet, wenn es in eine Datei oder einen Stream serialisiert wurde.

Die genaue Struktur des Markups ist für das XPS-om nicht verfügbar, wenn ein XPS-Dokument von einem Markup zu einem XPS-OM deserialisiert wird. Beispielsweise wird, unabhängig davon, ob die Eigenschaft als Element oder Attribut im Markup dargestellt wurde, der Eigenschafts Wert eines Dokument Objekts auf genau die gleiche Weise vom XPS-OM dargestellt.

Die [XPS-Dokument-API](documents-xps.md) kann in die folgenden Kategorien unterteilt werden:

-   [XPS-OM-trunk Schnittstellen](xps-om-trunk-interfaces.md)

    Die trunk Schnittstellen ermöglichen den Zugriff auf die Komponenten der obersten Ebene der XPS-Dokumentstruktur. Diese Schnittstellen bieten außerdem die Möglichkeit, ein XPS-OM zu serialisieren und ein XPS-Dokument zu deserialisieren.

-   [XPS-Schnittstellen für Schnittstellen](xps-object-model-page-interfaces.md)

    Die Seiten Schnittstellen ermöglichen den Zugriff auf den Inhalt einer Seite in einem XPS-Dokument. Die Schnittstellen, die den Inhalt der Seite beschreiben, sind auch in den Seiten Schnittstellen enthalten.

-   [Digitale XPS-OM-Signaturen](using-the-xps-digital-signatures.md)

    Das XPS-OM unterstützt digitale Signaturen. Sie können jedoch direkt auf digitale Signaturen in einem XPS-Dokument zugreifen, ohne ein XPS-OM erstellen zu müssen. Weitere Informationen zum Zugreifen auf XPS Digital Signaturen ohne XPS-OM finden Sie unter [XPS Digital Signature API](xps-digital-signatures.md).

-   [Schnittstellen für XPS-OM-Druck Tickets](xps-object-model-print-ticket-interfaces.md)

    XPS-Dokumente unterstützen Druck Tickets auf Paket-(Auftrags-), Dokument-und Seitenebene. Druck Tickets enthalten Informationen zum Formatieren von Dokument Inhalten zum Drucken oder anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**In diesem Abschnitt**
</dt> <dt>

[XPS-OM-trunk Schnittstellen](xps-om-trunk-interfaces.md)
</dt> <dt>

[XPS-Schnittstellen für Schnittstellen](xps-object-model-page-interfaces.md)
</dt> <dt>

[Digitale XPS-OM-Signaturen](using-the-xps-digital-signatures.md)
</dt> <dt>

[Schnittstellen für XPS-OM-Druck Tickets](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Weitere verwandte Themen**
</dt> <dt>

[Initialisieren eines XPS-OMS](xps-object-model-initialization.md)
</dt> <dt>

[Digitale XPS-OM-Signaturen](using-the-xps-digital-signatures.md)
</dt> <dt>

[XPS-Dokument-API-Referenz](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



