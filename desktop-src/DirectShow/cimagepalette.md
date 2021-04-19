---
description: Die cimagepalette-Klasse verwaltet Paletten für Videorenderer. Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen. Diese Klasse ist für die Verwendung mit den cbasewindow-und cdrawimage-Klassen vorgesehen, sodass Sie etwas spezieller ist.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Cimagepalette-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346386"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="42144-105">Cimagepalette-Klasse</span><span class="sxs-lookup"><span data-stu-id="42144-105">CImagePalette class</span></span>

<span data-ttu-id="42144-106">Die- `CImagePalette` Klasse verwaltet Paletten für Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="42144-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="42144-107">Sie kann verwendet werden, um eine logische Palette aus einem Videoformat zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42144-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="42144-108">Diese Klasse ist für die Verwendung mit den [**cbasewindow**](cbasewindow.md) -und [**cdrawimage**](cdrawimage.md) -Klassen vorgesehen, sodass Sie etwas spezieller ist.</span><span class="sxs-lookup"><span data-stu-id="42144-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="42144-109">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="42144-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="42144-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42144-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42144-111">**m \_ hpalette**</span><span class="sxs-lookup"><span data-stu-id="42144-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="42144-112">Handle für die logische Palette, die von diesem Objekt verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="42144-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="42144-113">**m \_ pbasewindow**</span><span class="sxs-lookup"><span data-stu-id="42144-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="42144-114">Zeiger auf das **cbasewindow** -Objekt, das das Fenster verwaltet.</span><span class="sxs-lookup"><span data-stu-id="42144-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="42144-115">**m \_ pdrawimage**</span><span class="sxs-lookup"><span data-stu-id="42144-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="42144-116">Zeiger auf das **cdrawimage** -Objekt, das das Videobild zeichnet.</span><span class="sxs-lookup"><span data-stu-id="42144-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="42144-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="42144-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="42144-118">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="42144-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="42144-119">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="42144-119">Public Methods</span></span>                                                   | <span data-ttu-id="42144-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42144-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="42144-121">**Cimagepalette**</span><span class="sxs-lookup"><span data-stu-id="42144-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="42144-122">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="42144-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="42144-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="42144-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="42144-124">Kopiert die Palette aus einer beliebigen **videoinfo** -Struktur in eine beliebige paletsierte **videoinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="42144-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="42144-125">**Makeidentitypalette**</span><span class="sxs-lookup"><span data-stu-id="42144-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="42144-126">Versucht, eine Palette zu erstellen, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="42144-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="42144-127">**Makepalette**</span><span class="sxs-lookup"><span data-stu-id="42144-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="42144-128">Erstellt eine logische Palette aus der Farbtabelle in einem Videoformat.</span><span class="sxs-lookup"><span data-stu-id="42144-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="42144-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="42144-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="42144-130">Richtet eine Palette auf der Grundlage eines Medientyps aus dem besitzenden Filter ein.</span><span class="sxs-lookup"><span data-stu-id="42144-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="42144-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="42144-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="42144-132">Löscht die vorhandene logische Palette.</span><span class="sxs-lookup"><span data-stu-id="42144-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



