---
description: Mehrere Bild Dateiformate ermöglichen es Ihnen, Metadaten zusammen mit einem Bild zu speichern.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Bildeigenschaften-tagkonstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979088"
---
# <a name="image-property-tag-constants"></a>Bildeigenschaften-tagkonstanten

Mehrere Bild Dateiformate ermöglichen es Ihnen, Metadaten zusammen mit einem Bild zu speichern. Metadaten sind Informationen zu einem Bild, z. b. Titel, Breite, Kameramodell und Künstler. Windows GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in den Formaten Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) und der austauschbaren Bilddatei (EXIF).

In GDI+ wird ein Metadatenelement als *Eigenschafts Element* bezeichnet, und ein einzelnes Eigenschaften Element wird durch eine numerische Konstante identifiziert, die als *Eigenschaftstag* bezeichnet wird. Sie können Metadaten speichern und abrufen, indem Sie die [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) -Methode und die [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, und Sie müssen sich nicht um die Details kümmern, wie ein bestimmtes Dateiformat diese Metadaten speichert.

In den folgenden Themen werden die von GDI+ unterstützten Eigenschaften Elemente aufgelistet und beschrieben. Die Beschreibungen sind kurz und allgemein, sodass Sie für eine Vielzahl von Dateiformaten gelten. Eine ausführliche Beschreibung der Verwendung eines Eigenschafts Elements in einem bestimmten Dateiformat finden Sie in der Spezifikation für dieses Dateiformat. Links zu verschiedenen Dateiformat Spezifikationen finden Sie unter [Spezifikationen des Image Datei Formats](-gdiplus-constant-image-file-format-specifications.md). Weitere Informationen zu Metadaten finden Sie unter [Lesen und Schreiben von Metadaten](-gdiplus-reading-and-writing-metadata-use.md) und [**Tagtyp Konstanten für Bildeigenschaften**](-gdiplus-constant-image-property-tag-type-constants.md).

-   [Eigenschaften Tags in numerischer Reihenfolge](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Eigenschaften Tags in alphabetischer Reihenfolge](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Eigenschaften Element Beschreibungen](-gdiplus-constant-property-item-descriptions.md)

 

 



