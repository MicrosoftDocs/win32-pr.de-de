---
description: DVD Subpicture-Eigenschaften steuern die Farbe, den Kontrast und die Ausgabe der Anzeige der Unterbilddatei.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: DVD Subpicture-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909088"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="f969a-103">DVD Subpicture-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="f969a-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="f969a-104">DVD Subpicture-Eigenschaften steuern die Farbe, den Kontrast und die Ausgabe der Anzeige der Unterbilddatei.</span><span class="sxs-lookup"><span data-stu-id="f969a-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="f969a-105">Die folgenden Informationen enthalten die erforderlichen Konstanten und Datentypen, die für diesen Eigenschaftensatz in Aufrufen von [**IKsPropertySet-Methoden**](ikspropertyset.md) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f969a-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="f969a-106">Sie stellt Werte für die **Parameter GUID** (*guidPropSet),* Eigenschaften-ID (*dwPropID*) und Eigenschaftendatentyp (*pPropData*) bereit.</span><span class="sxs-lookup"><span data-stu-id="f969a-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="f969a-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f969a-107">Label</span></span> | <span data-ttu-id="f969a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="f969a-108">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="f969a-109">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="f969a-109">Property Set GUID</span></span> | <span data-ttu-id="f969a-110">AM \_ KSPROPSETID \_ DvdSubPic</span><span class="sxs-lookup"><span data-stu-id="f969a-110">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="f969a-111">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="f969a-111">Property ID</span></span>                           | <span data-ttu-id="f969a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f969a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f969a-113">\_AM-EIGENSCHAFT \_ DVDSUBPIC \_ COMPOSIT \_ ON</span><span class="sxs-lookup"><span data-stu-id="f969a-113">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="f969a-114">Nur festlegende Eigenschaft, die die Anzeige der Unterbildanzeige aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f969a-114">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="f969a-115">DirectShow definiert den booleschen AM **\_ PROPERTY \_ COMPOSIT \_ ON-Datentyp** für diese Eigenschaft sowie PAM \_ PROPERTY \_ COMPOSIT \_ ON als Zeiger auf diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="f969a-115">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="f969a-116">**TRUE** gibt an, dass das Teilbild angezeigt wird, **FALSE** gibt an, dass es deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="f969a-116">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="f969a-117">Weitere Informationen finden Sie im WDM-Teil des Windows-DDK.</span><span class="sxs-lookup"><span data-stu-id="f969a-117">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="f969a-118">AM \_ PROPERTY \_ DVDSUBPIC \_ HLI</span><span class="sxs-lookup"><span data-stu-id="f969a-118">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="f969a-119">Nur festlegende Eigenschaft, die ein Rechteck aus Bildunterdrückung oder Bildschirm angibt, dessen Farbe oder Kontrast geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f969a-119">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="f969a-120">Der Datentyp ist [**AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli)</span><span class="sxs-lookup"><span data-stu-id="f969a-120">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="f969a-121">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f969a-121">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="f969a-122">AM \_ PROPERTY \_ DVDSUBPIC \_ PALETTE</span><span class="sxs-lookup"><span data-stu-id="f969a-122">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="f969a-123">Legt die Palette für ein Teilbild fest.</span><span class="sxs-lookup"><span data-stu-id="f969a-123">Sets the palette for a subpicture.</span></span> <span data-ttu-id="f969a-124">Der Datentyp ist [**AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)</span><span class="sxs-lookup"><span data-stu-id="f969a-124">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="f969a-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f969a-125">Remarks</span></span>

<span data-ttu-id="f969a-126">Die **EIGENSCHAFT AM PROPERTY \_ \_ DVDSUBPIC \_ HLI** ist nur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f969a-126">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="f969a-127">Sie gibt ein Rechteck aus Bildunterdrückung oder Bildschirm an, dessen Farbe oder Kontrast geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f969a-127">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="f969a-128">Dies unterscheidet sich von der DVD-Video-Spezifikation, da der Microsoft DVD-Navigator alle Schaltflächen- und Tastaturinformationen analysiert und zu einem bestimmten Zeitpunkt nur ein Hervorhebungrechteck an den Unterbilddecoder übergibt.</span><span class="sxs-lookup"><span data-stu-id="f969a-128">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="f969a-129">Daher werden Hervorhebungsinformationen häufiger an den Decoder gesendet, als sie im DVD-Stream vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f969a-129">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="f969a-130">Die Hervorhebungsinformationen werden asynchron im Datenstrom eintreffen.</span><span class="sxs-lookup"><span data-stu-id="f969a-130">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="f969a-131">Der Decoder verwendet die Hervorhebungs-Start- und Endzeitstempel, um die Hervorhebungsinformationen mit den relevanten Unterbildinformationen zu korrelieren, falls dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="f969a-131">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="f969a-132">Wenn der Decoder keine Unterbilddatenstrominformationen für die angeforderten Zeitstempel empfangen hat, geht der Decoder davon aus, dass die Hervorhebungsinformationen eigenständige sind und nicht für ein Unterbild gelten.</span><span class="sxs-lookup"><span data-stu-id="f969a-132">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="f969a-133">In diesem Fall geht der Decoder davon aus, dass die Farb- und Kontrastinformationen dieselbe Farbe haben.</span><span class="sxs-lookup"><span data-stu-id="f969a-133">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="f969a-134">Die Daten sind nicht vollständig im DVD-Datenträgerformat.</span><span class="sxs-lookup"><span data-stu-id="f969a-134">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="f969a-135">Microsoft stellt eine zusätzliche Struktur vom Typ [**AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) zur Verfügung, die als Parameter an diese Eigenschaft übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f969a-135">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="f969a-136">Diese Struktur beschreibt die aktuell ausgewählte Schaltfläche aus den Informationen zur DVD-Hervorhebung.</span><span class="sxs-lookup"><span data-stu-id="f969a-136">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="f969a-137">Der DVD-Navigator verarbeitet alle Tastatureingabeinformationen und sendet bei jeder Änderung eines Schaltflächenzustands neue Hervorhebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="f969a-137">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="f969a-138">Die Informationen beschreiben nur einen Modus von einer Schaltfläche gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="f969a-138">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="f969a-139">Sie enthält ein Anzeigerechteck in Pixelkoordinaten des Bildschirms oder eine Anzeige des Unterbilds, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f969a-139">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="f969a-140">Die -Struktur enthält auch Farb- und Kontrastinformationen, jedoch nur für den aktuellen Zustand der aktuell ausgewählten Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="f969a-140">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="f969a-141">Das Format wird in der DVD-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="f969a-141">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="f969a-142">Hervorhebungsinformationen enthalten Start- und Endzeitstempel.</span><span class="sxs-lookup"><span data-stu-id="f969a-142">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="f969a-143">Diese befinden sich in den gleichen Einheiten wie andere Zeitstempel, mit zwei Ausnahmen: Ein Startzeitstempel von 0xFFFFFFFF bedeutet, dass die Highlight-Eigenschaft beim Empfang wirksam ist, und ein Endzeitstempel von 0xFFFFFFFF bedeutet, dass die Highlight-Eigenschaft gültig ist, bis die nächste Hervorhebung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f969a-143">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="f969a-144">Das HLISS-Feld ist wie in der DVD-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="f969a-144">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="f969a-145">Der Wert 0 gibt an, dass alle Hervorhebungen ungültig sind, und der Decoder sollte alle Hervorhebungen deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f969a-145">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="f969a-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f969a-146">Requirements</span></span>



| <span data-ttu-id="f969a-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f969a-147">Requirement</span></span> | <span data-ttu-id="f969a-148">Wert</span><span class="sxs-lookup"><span data-stu-id="f969a-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f969a-149">Header</span><span class="sxs-lookup"><span data-stu-id="f969a-149">Header</span></span><br/> | <dl> <span data-ttu-id="f969a-150"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f969a-150"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f969a-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f969a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f969a-152">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="f969a-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




