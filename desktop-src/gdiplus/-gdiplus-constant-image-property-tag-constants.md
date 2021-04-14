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
# <a name="image-property-tag-constants"></a><span data-ttu-id="10033-103">Bildeigenschaften-tagkonstanten</span><span class="sxs-lookup"><span data-stu-id="10033-103">Image Property Tag Constants</span></span>

<span data-ttu-id="10033-104">Mehrere Bild Dateiformate ermöglichen es Ihnen, Metadaten zusammen mit einem Bild zu speichern.</span><span class="sxs-lookup"><span data-stu-id="10033-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="10033-105">Metadaten sind Informationen zu einem Bild, z. b. Titel, Breite, Kameramodell und Künstler.</span><span class="sxs-lookup"><span data-stu-id="10033-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="10033-106">Windows GDI+ bietet eine einheitliche Möglichkeit zum Speichern und Abrufen von Metadaten aus Bilddateien in den Formaten Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG) und der austauschbaren Bilddatei (EXIF).</span><span class="sxs-lookup"><span data-stu-id="10033-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="10033-107">In GDI+ wird ein Metadatenelement als *Eigenschafts Element* bezeichnet, und ein einzelnes Eigenschaften Element wird durch eine numerische Konstante identifiziert, die als *Eigenschaftstag* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="10033-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="10033-108">Sie können Metadaten speichern und abrufen, indem Sie die [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) -Methode und die [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) -Methode der [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufrufen, und Sie müssen sich nicht um die Details kümmern, wie ein bestimmtes Dateiformat diese Metadaten speichert.</span><span class="sxs-lookup"><span data-stu-id="10033-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="10033-109">In den folgenden Themen werden die von GDI+ unterstützten Eigenschaften Elemente aufgelistet und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="10033-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="10033-110">Die Beschreibungen sind kurz und allgemein, sodass Sie für eine Vielzahl von Dateiformaten gelten.</span><span class="sxs-lookup"><span data-stu-id="10033-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="10033-111">Eine ausführliche Beschreibung der Verwendung eines Eigenschafts Elements in einem bestimmten Dateiformat finden Sie in der Spezifikation für dieses Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="10033-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="10033-112">Links zu verschiedenen Dateiformat Spezifikationen finden Sie unter [Spezifikationen des Image Datei Formats](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="10033-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="10033-113">Weitere Informationen zu Metadaten finden Sie unter [Lesen und Schreiben von Metadaten](-gdiplus-reading-and-writing-metadata-use.md) und [**Tagtyp Konstanten für Bildeigenschaften**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="10033-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="10033-114">Eigenschaften Tags in numerischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="10033-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="10033-115">Eigenschaften Tags in alphabetischer Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="10033-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="10033-116">Eigenschaften Element Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="10033-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



