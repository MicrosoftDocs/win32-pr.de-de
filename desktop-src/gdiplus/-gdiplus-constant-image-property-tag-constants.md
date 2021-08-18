---
description: Mit mehreren Bilddateiformaten können Sie Metadaten zusammen mit einem Bild speichern.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Image-Eigenschaftentagkonst constants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509caf20659628909d225bb2dc34a4dbaa27047c08e361b28e9777141f213751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696418"
---
# <a name="image-property-tag-constants"></a>Image-Eigenschaftentagkonst constants

Mit mehreren Bilddateiformaten können Sie Metadaten zusammen mit einem Bild speichern. Metadaten sind Informationen zu einem Bild, z. B. Titel, Breite, Kameramodell und Interpret. Windows GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in den Formaten Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) und Exchangeable Image File (EXIF).

In GDI+ wird ein Metadatenelement als Eigenschaftenelement bezeichnet, und ein einzelnes Eigenschaftenelement wird durch eine numerische Konstante identifiziert, die als *Eigenschaftentag bezeichnet wird.* Sie können Metadaten speichern und abrufen, indem Sie die [**Methoden Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) und [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) der [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen, und Sie müssen sich nicht um die Details der Speicherung dieser Metadaten in einem bestimmten Dateiformat sorgen.

In den folgenden Themen werden die eigenschaftenelemente aufgeführt und beschrieben, die von GDI+. Die Beschreibungen sind kurz und allgemein, sodass sie für eine Vielzahl von Dateiformaten gelten. Eine ausführliche Beschreibung der Verwendung eines Eigenschaftenelements in einem bestimmten Dateiformat finden Sie in der Spezifikation für dieses Dateiformat. Links zu verschiedenen Dateiformatspezifikationen finden Sie unter [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md). Weitere Informationen zu Metadaten finden Sie unter Lesen und Schreiben [von Metadaten und](-gdiplus-reading-and-writing-metadata-use.md) [**Tagtypkonst constants der Bildeigenschaft.**](-gdiplus-constant-image-property-tag-type-constants.md)

-   [Eigenschaftstags in numerischer Reihenfolge](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [Eigenschaftstags in alphabetischer Reihenfolge](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [Eigenschaftenelementbeschreibungen](-gdiplus-constant-property-item-descriptions.md)

 

 



