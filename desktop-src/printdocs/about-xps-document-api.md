---
description: Die XPS-Dokument-API implementiert das XPS-Objektmodell und ermöglicht Es Entwicklern, eine XPS OM zu erstellen, XPS-Dokumentinhalte in nativen Windows Programmen zu bearbeiten \\ \\ und die XPS OM in einer Datei oder einem Stream als XPS-Dokument zu speichern.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informationen zur XPS-Dokument-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b2363bba55fed184b1cf80bfc81fac9474444f77c9b867b461940e6b72d8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950910"
---
# <a name="about-xps-document-api"></a>Informationen zur XPS-Dokument-API

Die [XPS-Dokument-API](documents-xps.md) implementiert das XPS-Objektmodell und ermöglicht Es Entwicklern, eine XPS OM zu erstellen, XPS-Dokumentinhalte in nativen Windows Programmen zu bearbeiten \\ \\ und das XPS OM in einer Datei oder einem Stream als XPS-Dokument zu speichern. Entwickler von XPSDrv-Filterpipelinemodulen können auch die XPS-Dokument-API verwenden, um XPS-Dokumentinhalte in einem XPSDrv-Druckertreiberfilter zu bearbeiten.

## <a name="xps-document-api-overview"></a>Übersicht über die XPS-Dokument-API

Das XPS-Objektmodell ist das Informationsmodell eines XPS-Dokuments. Das Informationsmodell des XPS-Dokuments ist vom Markupmodell getrennt, das in den Dokumentteilen verwendet wird. Das XPS-Objektmodell beschreibt die Organisation der internen Komponenten, aus denen ein XPS-Dokument besteht, und das Markupmodell beschreibt den Inhalt dieser Komponenten.

In einem Programm wird das XPS-Objektmodell als XPS OM instanziiert. Die XPS OM ist im Wesentlichen eine In-Memory-Version des Inhalts eines XPS-Dokuments. Obwohl ein XPS OM in der logischen Organisation einem XPS-Dokument ähnelt, wird es erst dann als XPS-Dokument betrachtet, wenn es in eine Datei oder einen Stream serialisiert wurde.

Die genaue Struktur des Markups ist für XPS OM nicht verfügbar, wenn ein XPS-Dokument vom Markup in ein XPS OM deserialisiert wird. Unabhängig davon, ob die Eigenschaft als Element oder Attribut im Markup dargestellt wurde, wird der Eigenschaftswert eines Dokumentobjekts vom XPS OM auf genau die gleiche Weise dargestellt.

Die [XPS-Dokument-API](documents-xps.md) kann in die folgenden Kategorien unterteilt werden:

-   [XPS OM-Trunkschnittstellen](xps-om-trunk-interfaces.md)

    Die Trunkschnittstellen bieten Zugriff auf die Komponenten der obersten Ebene der XPS-Dokumentstruktur. Diese Schnittstellen bieten auch die Möglichkeit, ein XPS OM zu serialisieren und ein XPS-Dokument zu deserialisieren.

-   [XPS OM-Seitenschnittstellen](xps-object-model-page-interfaces.md)

    Die Seitenschnittstellen bieten Zugriff auf den Inhalt einer Seite in einem XPS-Dokument. Die Schnittstellen, die den Inhalt der Seite beschreiben, sind auch in den Seitenschnittstellen enthalten.

-   [Digitale XPS OM-Signaturen](using-the-xps-digital-signatures.md)

    XPS OM unterstützt digitale Signaturen. Sie können jedoch direkt auf digitale Signaturen in einem XPS-Dokument zugreifen, ohne eine XPS OM zu erstellen. Weitere Informationen zum Zugriff auf digitale XPS-Signaturen ohne XPS OM finden Sie unter [XPS Digital Signature API](xps-digital-signatures.md).

-   [XPS OM– Druckticketschnittstellen](xps-object-model-print-ticket-interfaces.md)

    XPS-Dokumente unterstützen das Drucken von Tickets auf Paket-, Dokument- und Seitenebene. Drucktickets enthalten Informationen zum Formatieren von Dokumentinhalten zum Drucken oder Anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**In diesem Abschnitt**
</dt> <dt>

[XPS OM-Trunkschnittstellen](xps-om-trunk-interfaces.md)
</dt> <dt>

[XPS OM-Seitenschnittstellen](xps-object-model-page-interfaces.md)
</dt> <dt>

[Digitale XPS OM-Signaturen](using-the-xps-digital-signatures.md)
</dt> <dt>

[XPS OM– Druckticketschnittstellen](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

**Weitere verwandte Themen**
</dt> <dt>

[Initialisieren einer XPS OM](xps-object-model-initialization.md)
</dt> <dt>

[Digitale XPS OM-Signaturen](using-the-xps-digital-signatures.md)
</dt> <dt>

[REFERENZ ZUR XPS-Dokument-API](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



