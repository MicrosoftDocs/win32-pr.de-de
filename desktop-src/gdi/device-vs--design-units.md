---
description: Eine Anwendung kann Schriftart Metriken nur für eine physische Schriftart abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde.
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: Geräte im Vergleich zu Entwurfs Einheiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863660"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="802a4-103">Geräte im Vergleich zu Entwurfs Einheiten</span><span class="sxs-lookup"><span data-stu-id="802a4-103">Device vs. Design Units</span></span>

<span data-ttu-id="802a4-104">Eine Anwendung kann Schriftart Metriken nur für eine physische Schriftart abrufen, nachdem die Schriftart in einem Gerätekontext ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="802a4-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="802a4-105">Wenn eine Schriftart in einen Gerätekontext ausgewählt wird, wird Sie für das Gerät skaliert.</span><span class="sxs-lookup"><span data-stu-id="802a4-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="802a4-106">Die für das Gerät spezifischen Schriftart Metriken werden als Geräte Einheiten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="802a4-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="802a4-107">Portable Metriken in Schriftarten werden als Entwurfs Einheiten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="802a4-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="802a4-108">Entwurfs Einheiten müssen in Geräte Einheiten konvertiert werden, damit Sie auf ein bestimmtes Gerät angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="802a4-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="802a4-109">Verwenden Sie die folgende Formel, um Entwurfs Einheiten in Geräte Einheiten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="802a4-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="802a4-110">*Deviceunits* = (*designunits* / *unitsperem*) \* (*pointsize*/72) \* *deviceresolution*</span><span class="sxs-lookup"><span data-stu-id="802a4-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="802a4-111">Die Variablen in dieser Formel haben folgende Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="802a4-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="802a4-112">Variable</span><span class="sxs-lookup"><span data-stu-id="802a4-112">Variable</span></span>           | <span data-ttu-id="802a4-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="802a4-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="802a4-114">*Deviceunits*</span><span class="sxs-lookup"><span data-stu-id="802a4-114">*DeviceUnits*</span></span>      | <span data-ttu-id="802a4-115">Gibt die in Geräte Einheiten konvertierte Schriftart Metrik " *designunits* " an.</span><span class="sxs-lookup"><span data-stu-id="802a4-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="802a4-116">Dieser Wert befindet sich in den gleichen Einheiten wie der für *deviceresolution* angegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="802a4-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="802a4-117">*Design Units*</span><span class="sxs-lookup"><span data-stu-id="802a4-117">*DesignUnits*</span></span>      | <span data-ttu-id="802a4-118">Gibt die Schriftart Metrik an, die in Geräte Einheiten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="802a4-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="802a4-119">Bei diesem Wert kann es sich um eine beliebige Schriftart Metrik handeln, einschließlich der Breite eines Zeichens oder des aufsteigenden Werts für eine ganze Schriftart.</span><span class="sxs-lookup"><span data-stu-id="802a4-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="802a4-120">*unitsperem*</span><span class="sxs-lookup"><span data-stu-id="802a4-120">*unitsPerEm*</span></span>       | <span data-ttu-id="802a4-121">Gibt die EM-Quadrat Größe für die Schriftart an.</span><span class="sxs-lookup"><span data-stu-id="802a4-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="802a4-122">*PointSize*</span><span class="sxs-lookup"><span data-stu-id="802a4-122">*PointSize*</span></span>        | <span data-ttu-id="802a4-123">Gibt die Schriftgröße in Punkt an.</span><span class="sxs-lookup"><span data-stu-id="802a4-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="802a4-124">(Ein Punkt ist gleich 1/72 Zoll.)</span><span class="sxs-lookup"><span data-stu-id="802a4-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="802a4-125">*Deviceresolution*</span><span class="sxs-lookup"><span data-stu-id="802a4-125">*DeviceResolution*</span></span> | <span data-ttu-id="802a4-126">Gibt die Anzahl der Geräte Einheiten (Pixel) pro Zoll an.</span><span class="sxs-lookup"><span data-stu-id="802a4-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="802a4-127">Typische Werte können 300 für einen Laserdrucker oder 96 für einen VGA-Bildschirm sein.</span><span class="sxs-lookup"><span data-stu-id="802a4-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="802a4-128">Diese Formel sollte nicht verwendet werden, um Geräte Einheiten zurück in Entwurfs Einheiten zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="802a4-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="802a4-129">Geräte Einheiten werden immer auf das nächste Pixel gerundet.</span><span class="sxs-lookup"><span data-stu-id="802a4-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="802a4-130">Der weitergaberoundfehler kann sehr groß werden, insbesondere dann, wenn eine Anwendung mit Bildschirmgrößen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="802a4-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="802a4-131">Um Entwurfs Einheiten anzufordern, erstellen Sie eine logische Schriftart, deren Höhe als *unitsperem* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="802a4-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="802a4-132">Anwendungen können den Wert für *unitsperem* abrufen, indem Sie die Funktion " [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) " aufrufen und den **ntmsizeem** -Member der [**newtextmetric**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) -Struktur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="802a4-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



