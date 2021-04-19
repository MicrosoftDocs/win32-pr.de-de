---
title: Standard-DispIds
description: Es wurden eine Reihe von Standard-DISPIDs für die Steuerelement Spezifikation definiert.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341439"
---
# <a name="standard-dispids"></a><span data-ttu-id="d8b7c-103">Standard-DispIds</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">Standard DISPIDS</span></span>

<span data-ttu-id="d8b7c-104">Es wurden eine Reihe von Standard-DISPIDs für die Steuerelement Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">A number of standard dispids have been defined for the controls specification.</span></span>

## <a name="dispid_mousepointer"></a><span data-ttu-id="d8b7c-105">DISPID- \_ mouum Zeiger</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">DISPID\_MOUSEPOINTER</span></span>

<span data-ttu-id="d8b7c-106">Eigenschaft vom Typ Integer.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">Property of type integer.</span></span>

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

<span data-ttu-id="d8b7c-107">Die MousePointer-Eigenschaft identifiziert Standard Maus Symbole.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">The Mousepointer property identifies standard mouse icons.</span></span>



| <span data-ttu-id="d8b7c-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">Value</span></span>         | <span data-ttu-id="d8b7c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">Description</span></span>                                                                |
|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d8b7c-110">0</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">0</span></span><br/>  | <span data-ttu-id="d8b7c-111">Vorgegebene Die vom-Objekt festgelegte Form.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">(Default) Shape determined by the object.</span></span><br/>                       |
| <span data-ttu-id="d8b7c-112">1</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">1</span></span><br/>  | <span data-ttu-id="d8b7c-113">Pfeil</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">Arrow</span></span><br/>                                                           |
| <span data-ttu-id="d8b7c-114">2</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">2</span></span><br/>  | <span data-ttu-id="d8b7c-115">Kreuz (Kreuz-Mauszeiger)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">Cross (cross-hair pointer)</span></span><br/>                                      |
| <span data-ttu-id="d8b7c-116">3</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">3</span></span><br/>  | <span data-ttu-id="d8b7c-117">I-Strahl</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">I Beam</span></span><br/>                                                          |
| <span data-ttu-id="d8b7c-118">4</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">4</span></span><br/>  | <span data-ttu-id="d8b7c-119">Symbol (kleines Quadrat innerhalb eines Quadrats)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">Icon (small square within a square)</span></span><br/>                             |
| <span data-ttu-id="d8b7c-120">5</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">5</span></span><br/>  | <span data-ttu-id="d8b7c-121">Größe (vier-Spitze-Pfeil, der nach Nord, Süd, Ost und West zeigt)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">Size (four-pointed arrow pointing north, south, east, and west)</span></span><br/> |
| <span data-ttu-id="d8b7c-122">6</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">6</span></span><br/>  | <span data-ttu-id="d8b7c-123">Größe ne SW (doppelter Pfeil, der auf Nordost und Südwest zeigt)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">Size NE SW (double arrow pointing northeast and southwest)</span></span><br/>      |
| <span data-ttu-id="d8b7c-124">7</span><span class="sxs-lookup"><span data-stu-id="d8b7c-124">7</span></span><br/>  | <span data-ttu-id="d8b7c-125">Größe N S (doppelter Pfeil, der nach Norden und Süden zeigt)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-125">Size N S (double arrow pointing north and south)</span></span><br/>                |
| <span data-ttu-id="d8b7c-126">8</span><span class="sxs-lookup"><span data-stu-id="d8b7c-126">8</span></span><br/>  | <span data-ttu-id="d8b7c-127">Größe NW, SE</span><span class="sxs-lookup"><span data-stu-id="d8b7c-127">Size NW, SE</span></span><br/>                                                     |
| <span data-ttu-id="d8b7c-128">9</span><span class="sxs-lookup"><span data-stu-id="d8b7c-128">9</span></span><br/>  | <span data-ttu-id="d8b7c-129">Größe E W (doppelter Pfeil, der nach Osten und Westen zeigt)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-129">Size E W (double arrow pointing east and west)</span></span><br/>                  |
| <span data-ttu-id="d8b7c-130">10</span><span class="sxs-lookup"><span data-stu-id="d8b7c-130">10</span></span><br/> | <span data-ttu-id="d8b7c-131">NACH-OBEN</span><span class="sxs-lookup"><span data-stu-id="d8b7c-131">Up Arrow</span></span><br/>                                                        |
| <span data-ttu-id="d8b7c-132">11</span><span class="sxs-lookup"><span data-stu-id="d8b7c-132">11</span></span><br/> | <span data-ttu-id="d8b7c-133">Sanduhr (warten)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-133">Hourglass (wait)</span></span><br/>                                                |
| <span data-ttu-id="d8b7c-134">12</span><span class="sxs-lookup"><span data-stu-id="d8b7c-134">12</span></span><br/> | <span data-ttu-id="d8b7c-135">Kein Drop</span><span class="sxs-lookup"><span data-stu-id="d8b7c-135">No Drop</span></span><br/>                                                         |
| <span data-ttu-id="d8b7c-136">13</span><span class="sxs-lookup"><span data-stu-id="d8b7c-136">13</span></span><br/> | <span data-ttu-id="d8b7c-137">Pfeil und Sanduhr</span><span class="sxs-lookup"><span data-stu-id="d8b7c-137">Arrow and hourglass</span></span><br/>                                             |
| <span data-ttu-id="d8b7c-138">14</span><span class="sxs-lookup"><span data-stu-id="d8b7c-138">14</span></span><br/> | <span data-ttu-id="d8b7c-139">Pfeil und Fragezeichen</span><span class="sxs-lookup"><span data-stu-id="d8b7c-139">Arrow and question mark</span></span><br/>                                         |
| <span data-ttu-id="d8b7c-140">15</span><span class="sxs-lookup"><span data-stu-id="d8b7c-140">15</span></span><br/> | <span data-ttu-id="d8b7c-141">Größe alle</span><span class="sxs-lookup"><span data-stu-id="d8b7c-141">Size all</span></span><br/>                                                        |
| <span data-ttu-id="d8b7c-142">99</span><span class="sxs-lookup"><span data-stu-id="d8b7c-142">99</span></span><br/> | <span data-ttu-id="d8b7c-143">Durch die MouseIcon-Eigenschaft angegebenes benutzerdefiniertes Symbol</span><span class="sxs-lookup"><span data-stu-id="d8b7c-143">Custom icon specified by the MouseIcon property</span></span><br/>                 |



 

## <a name="dispid_mouseicon"></a><span data-ttu-id="d8b7c-144">DISPID \_ MouseIcon</span><span class="sxs-lookup"><span data-stu-id="d8b7c-144">DISPID\_MOUSEICON</span></span>

<span data-ttu-id="d8b7c-145">-Eigenschaft des Typs "Bild".</span><span class="sxs-lookup"><span data-stu-id="d8b7c-145">Property of type picture.</span></span>

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a><span data-ttu-id="d8b7c-146">DISPID- \_ Bild</span><span class="sxs-lookup"><span data-stu-id="d8b7c-146">DISPID\_PICTURE</span></span>

<span data-ttu-id="d8b7c-147">-Eigenschaft des Typs "Bild".</span><span class="sxs-lookup"><span data-stu-id="d8b7c-147">Property of type picture.</span></span>

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a><span data-ttu-id="d8b7c-148">DISPID \_ gültig</span><span class="sxs-lookup"><span data-stu-id="d8b7c-148">DISPID\_VALID</span></span>

<span data-ttu-id="d8b7c-149">Wird verwendet, um zu bestimmen, ob das Steuerelement über gültige Daten verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-149">Used to determine if the control has valid data or not.</span></span>

<span data-ttu-id="d8b7c-150">-Eigenschaft vom Typ bool.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-150">Property of type BOOL.</span></span>

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a><span data-ttu-id="d8b7c-151">"DISPID \_ AMBIENT \_ Palette"</span><span class="sxs-lookup"><span data-stu-id="d8b7c-151">DISPID\_ AMBIENT\_PALETTE</span></span>

<span data-ttu-id="d8b7c-152">Wird verwendet, um dem Steuerelement zu ermöglichen, den hpal des Containers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-152">Used to allow the control to get the container's HPAL.</span></span> <span data-ttu-id="d8b7c-153">Wenn der Container eine Ambient-Palette liefert, ist dies die einzige Palette, die möglicherweise im Vordergrund erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-153">If the container supplies an ambient palette then that is the only palette that may be realized into the foreground.</span></span> <span data-ttu-id="d8b7c-154">Steuerelemente, die ihre eigenen Paletten erkennen möchten, müssen dies im Hintergrund tun.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-154">Controls that want to realize their own palettes must do so in the background.</span></span> <span data-ttu-id="d8b7c-155">Wenn keine Ambient-Palette durch den Container bereitgestellt wird, kann das aktive Steuerelement seine Palette im Vordergrund erkennen.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-155">If there is no ambient palette provided by the container, then the active control can realize its palette in the foreground.</span></span> <span data-ttu-id="d8b7c-156">Die palettenbehandlung wird im Palette-Verhalten für OLE-Steuerelemente, die sich im ActiveX SDK befinden, ausführlicher erläutert.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-156">Palette handling is further discussed in Palette Behavior for OLE Controls which is in the ActiveX SDK.</span></span>

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





