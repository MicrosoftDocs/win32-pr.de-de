---
description: Die CursorType-Eigenschaft legt den aktuellen Cursortyp fest oder ruft ihn ab.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Cursor Type (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860286"
---
# <a name="cursortype-property"></a><span data-ttu-id="b1c42-103">Cursor Type (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1c42-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="b1c42-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1c42-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b1c42-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b1c42-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b1c42-106">Die- `CursorType` Eigenschaft legt den aktuellen Cursortyp fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b1c42-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="b1c42-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1c42-107">Return Value</span></span>

<span data-ttu-id="b1c42-108">Gibt einen Integer-Wert zurück, der den Cursortyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1c42-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1c42-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1c42-109">Remarks</span></span>

<span data-ttu-id="b1c42-110">Folgende Werte sind für diese Eigenschaft möglich:</span><span class="sxs-lookup"><span data-stu-id="b1c42-110">The possible values for this property are:</span></span>



| <span data-ttu-id="b1c42-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b1c42-111">Value</span></span> | <span data-ttu-id="b1c42-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1c42-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="b1c42-113">0</span><span class="sxs-lookup"><span data-stu-id="b1c42-113">0</span></span>     | <span data-ttu-id="b1c42-114">Pfeil</span><span class="sxs-lookup"><span data-stu-id="b1c42-114">Arrow</span></span>       |
| <span data-ttu-id="b1c42-115">1</span><span class="sxs-lookup"><span data-stu-id="b1c42-115">1</span></span>     | <span data-ttu-id="b1c42-116">Vergrößern</span><span class="sxs-lookup"><span data-stu-id="b1c42-116">Zoom In</span></span>     |
| <span data-ttu-id="b1c42-117">2</span><span class="sxs-lookup"><span data-stu-id="b1c42-117">2</span></span>     | <span data-ttu-id="b1c42-118">Verkleinern</span><span class="sxs-lookup"><span data-stu-id="b1c42-118">Zoom Out</span></span>    |
| <span data-ttu-id="b1c42-119">3</span><span class="sxs-lookup"><span data-stu-id="b1c42-119">3</span></span>     | <span data-ttu-id="b1c42-120">Linken</span><span class="sxs-lookup"><span data-stu-id="b1c42-120">Hand</span></span>        |
| <span data-ttu-id="b1c42-121">-1</span><span class="sxs-lookup"><span data-stu-id="b1c42-121">-1</span></span>    | <span data-ttu-id="b1c42-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b1c42-122">None</span></span>        |



 

<span data-ttu-id="b1c42-123">Diese Eigenschaft ist Lese-/Schreibzugriff mit dem Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b1c42-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="b1c42-124">Wenn das Bild vergrößert wird, wird die Anwendung durch die Festlegung `CursorType` auf **Hand** (0x3) in den Zieh Modus versetzt, sodass der Benutzer das Bild innerhalb des Videoanzeige Bereichs verschieben kann.</span><span class="sxs-lookup"><span data-stu-id="b1c42-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



