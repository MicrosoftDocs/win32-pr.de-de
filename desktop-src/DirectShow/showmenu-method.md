---
description: Die showmenu-Methode zeigt das angegebene Menü auf dem Bildschirm an.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Showmenu-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746785"
---
# <a name="showmenu-method"></a><span data-ttu-id="8f51f-103">Showmenu-Methode</span><span class="sxs-lookup"><span data-stu-id="8f51f-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="8f51f-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8f51f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8f51f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="8f51f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8f51f-106">Die- `ShowMenu` Methode zeigt das angegebene Menü auf dem Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="8f51f-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="8f51f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f51f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f51f-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*imumuid*</span><span class="sxs-lookup"><span data-stu-id="8f51f-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="8f51f-109">Gibt die Menü-ID als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="8f51f-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="8f51f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8f51f-110">Value</span></span> | <span data-ttu-id="8f51f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f51f-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="8f51f-112">2</span><span class="sxs-lookup"><span data-stu-id="8f51f-112">2</span></span>     | <span data-ttu-id="8f51f-113">Titel (oben)</span><span class="sxs-lookup"><span data-stu-id="8f51f-113">Title (Top)</span></span> |
| <span data-ttu-id="8f51f-114">3</span><span class="sxs-lookup"><span data-stu-id="8f51f-114">3</span></span>     | <span data-ttu-id="8f51f-115">Root</span><span class="sxs-lookup"><span data-stu-id="8f51f-115">Root</span></span>        |
| <span data-ttu-id="8f51f-116">4</span><span class="sxs-lookup"><span data-stu-id="8f51f-116">4</span></span>     | <span data-ttu-id="8f51f-117">Untertitel</span><span class="sxs-lookup"><span data-stu-id="8f51f-117">Subpicture</span></span>  |
| <span data-ttu-id="8f51f-118">5</span><span class="sxs-lookup"><span data-stu-id="8f51f-118">5</span></span>     | <span data-ttu-id="8f51f-119">Audio</span><span class="sxs-lookup"><span data-stu-id="8f51f-119">Audio</span></span>       |
| <span data-ttu-id="8f51f-120">6</span><span class="sxs-lookup"><span data-stu-id="8f51f-120">6</span></span>     | <span data-ttu-id="8f51f-121">Angle</span><span class="sxs-lookup"><span data-stu-id="8f51f-121">Angle</span></span>       |
| <span data-ttu-id="8f51f-122">7</span><span class="sxs-lookup"><span data-stu-id="8f51f-122">7</span></span>     | <span data-ttu-id="8f51f-123">Kapitel</span><span class="sxs-lookup"><span data-stu-id="8f51f-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f51f-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f51f-124">Return Value</span></span>

<span data-ttu-id="8f51f-125">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8f51f-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f51f-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f51f-126">Remarks</span></span>

<span data-ttu-id="8f51f-127">DVD-Menü Namen können etwas verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="8f51f-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="8f51f-128">Das Menü Titel ist ein anderer Name für das Menü Video-Manager, das Hauptmenü für die gesamte CD. im Allgemeinen werden alle auf der Festplatte verfügbaren Videotitel Sätze aufgelistet. Das Stamm Menü ist das Menü für einen Videotitel Satz, der einen Titel oder eine Gruppe von Titeln enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="8f51f-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="8f51f-129">Alle Titel in einem Titel Satz verwenden dieselben unter Bilder, Audiodateien und Winkel Menüs.</span><span class="sxs-lookup"><span data-stu-id="8f51f-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



