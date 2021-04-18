---
description: Die Eigenschaften des DVD-Teil Bilds steuern die Farbe, den Kontrast und die Ausgabe der Anzeige des unter Bilds.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Eigenschaften Satz des DVD-Teil Bilds (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371166"
---
# <a name="dvd-subpicture-property-set"></a><span data-ttu-id="4db5e-103">Eigenschaften Satz des DVD-Teil Bilds</span><span class="sxs-lookup"><span data-stu-id="4db5e-103">DVD Subpicture Property Set</span></span>

<span data-ttu-id="4db5e-104">Die Eigenschaften des DVD-Teil Bilds steuern die Farbe, den Kontrast und die Ausgabe der Anzeige des unter Bilds.</span><span class="sxs-lookup"><span data-stu-id="4db5e-104">DVD Subpicture properties control the color, contrast, and output of the subpicture display.</span></span>

<span data-ttu-id="4db5e-105">Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen dar, die für diesen Eigenschaften Satz in Aufrufen von " [**ikspropertyset**](ikspropertyset.md) "-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4db5e-105">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="4db5e-106">Es werden Werte für die Parameter **GUID** (*guidpropset*), Property ID (*dwpropid*) und Property Data Type (*ppropdata*) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4db5e-106">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="4db5e-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="4db5e-107">Property Set GUID</span></span> | <span data-ttu-id="4db5e-108">AM \_ kspropabtid \_ dvdsubpic</span><span class="sxs-lookup"><span data-stu-id="4db5e-108">AM\_KSPROPSETID\_DvdSubPic</span></span> |



 



| <span data-ttu-id="4db5e-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="4db5e-109">Property ID</span></span>                           | <span data-ttu-id="4db5e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4db5e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db5e-111">am- \_ Eigenschaft \_ dvdsubpic \_ Composit \_ on</span><span class="sxs-lookup"><span data-stu-id="4db5e-111">AM\_PROPERTY\_DVDSUBPIC\_COMPOSIT\_ON</span></span> | <span data-ttu-id="4db5e-112">Nur festgelegte Eigenschaft, die die Anzeige von Teil Bildern aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4db5e-112">Set-only property that enables or disables subpicture display.</span></span> <span data-ttu-id="4db5e-113">DirectShow definiert das **am- \_ Eigenschafts \_ Composit \_** für den booleschen Datentyp für diese Eigenschaft sowie die PAM- \_ Eigenschaft \_ Composit \_ als Zeiger auf diesen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="4db5e-113">DirectShow defines the **AM\_PROPERTY\_COMPOSIT\_ON** Boolean data type for this property, as well as PAM\_PROPERTY\_COMPOSIT\_ON as a pointer to this data type.</span></span> <span data-ttu-id="4db5e-114">**True** gibt an, dass das Unterbild angezeigt wird, **false** gibt an, dass es deaktiviert</span><span class="sxs-lookup"><span data-stu-id="4db5e-114">**TRUE** indicates display the subpicture, **FALSE** indicates disable it.</span></span> <span data-ttu-id="4db5e-115">Weitere Informationen finden Sie im WDM-Teil des Windows-DDK.</span><span class="sxs-lookup"><span data-stu-id="4db5e-115">See the WDM portion of the Windows DDK for more information.</span></span> |
| <span data-ttu-id="4db5e-116">AM- \_ Eigenschaft \_ dvdsubpic \_ HLI</span><span class="sxs-lookup"><span data-stu-id="4db5e-116">AM\_PROPERTY\_DVDSUBPIC\_HLI</span></span>          | <span data-ttu-id="4db5e-117">Nur festgelegte Eigenschaft, die ein Rechteck eines unter Bilds oder eines Bildschirms angibt, dessen Farbe oder Kontrast geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4db5e-117">Set-only property that specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="4db5e-118">Der Datentyp ist die [**\_ Eigenschaft \_ sphli**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span><span class="sxs-lookup"><span data-stu-id="4db5e-118">Data type is [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli).</span></span> <span data-ttu-id="4db5e-119">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="4db5e-119">See Remarks.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="4db5e-120">AM- \_ Eigenschaft ( \_ dvdsubpic- \_ Palette)</span><span class="sxs-lookup"><span data-stu-id="4db5e-120">AM\_PROPERTY\_DVDSUBPIC\_PALETTE</span></span>      | <span data-ttu-id="4db5e-121">Legt die Palette für ein Teilbild fest.</span><span class="sxs-lookup"><span data-stu-id="4db5e-121">Sets the palette for a subpicture.</span></span> <span data-ttu-id="4db5e-122">Der Datentyp ist die [**\_ Eigenschaft \_ sppal**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span><span class="sxs-lookup"><span data-stu-id="4db5e-122">Data type is [**AM\_PROPERTY\_SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).</span></span>                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="4db5e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4db5e-123">Remarks</span></span>

<span data-ttu-id="4db5e-124">Die Eigenschaft "an **\_ Eigenschaft \_ dvdsubpic \_ HLI** " ist nur festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4db5e-124">The **AM\_PROPERTY\_DVDSUBPIC\_HLI** property is set-only.</span></span> <span data-ttu-id="4db5e-125">Es gibt ein Rechteck mit einem unter Bild oder Bildschirm an, dessen Farbe oder Kontrast geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4db5e-125">It specifies a rectangle of subpicture or screen whose color or contrast will be changed.</span></span> <span data-ttu-id="4db5e-126">Dies unterscheidet sich von der DVD-Video Spezifikation, da der Microsoft DVD Navigator alle Schaltflächen-und Tastatur Informationen analysiert und jeweils nur ein Hervorhebungs Rechteck an den Teil Bild Decoder übergibt.</span><span class="sxs-lookup"><span data-stu-id="4db5e-126">This differs from the DVD-Video specification, in that the Microsoft DVD navigator parses all button and keyboard information and passes only one highlight rectangle to the subpicture decoder at any given time.</span></span> <span data-ttu-id="4db5e-127">Daher werden Hervorhebungs Informationen häufiger an den Decoder gesendet, als Sie im DVD-Stream vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4db5e-127">As a result, highlight information is sent to the decoder more often than it is present in the DVD stream.</span></span>

<span data-ttu-id="4db5e-128">Die Hervorhebungs Informationen werden asynchron in den Datenstrom gelangt.</span><span class="sxs-lookup"><span data-stu-id="4db5e-128">The highlight information arrives asynchronously to the data stream.</span></span> <span data-ttu-id="4db5e-129">Der Decoder verwendet die Hervorhebungs-und Endzeit Stempel, um die Hervorhebungs Informationen mit den entsprechenden Teil Bildinformationen zu korrelieren, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4db5e-129">The decoder uses the highlight Start and End time stamps to correlate the highlight information to the relevant subpicture information, if any.</span></span> <span data-ttu-id="4db5e-130">Wenn der Decoder keine unter bildstreaminformationen für die angeforderten Zeitstempel erhalten hat, geht der Decoder davon aus, dass die Hervorhebungs Informationen eigenständig sind und nicht auf ein Teilbild angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="4db5e-130">If the decoder has not received any subpicture stream information for the requested time stamps, the decoder assumes that the highlight information is stand-alone and does not apply to a subpicture.</span></span> <span data-ttu-id="4db5e-131">In diesem Fall geht der Decoder davon aus, dass die Farbe und die Kontrast Informationen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4db5e-131">In this case, the decoder assumes the color and contrast information is all the same color.</span></span>

<span data-ttu-id="4db5e-132">Die Daten sind nicht vollständig im DVD-Festplatten Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="4db5e-132">The data is not entirely in DVD disc format.</span></span> <span data-ttu-id="4db5e-133">Microsoft stellt eine zusätzliche Struktur des Typs " [**am \_ Property \_ sphli**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) " bereit, die als Parameter an diese Eigenschaft übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4db5e-133">Microsoft provides an additional structure of type [**AM\_PROPERTY\_SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) that is passed as the parameter to this property.</span></span> <span data-ttu-id="4db5e-134">Diese Struktur beschreibt die aktuell ausgewählte Schaltfläche aus den Informationen zur DVD-Hervorhebung.</span><span class="sxs-lookup"><span data-stu-id="4db5e-134">This structure describes the currently selected button from the DVD highlight information.</span></span>

<span data-ttu-id="4db5e-135">Der DVD-Navigator verarbeitet alle Tastatureingabe-Informationen und sendet bei jeder Änderung eines Schaltflächen Zustands neue Hervorhebungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="4db5e-135">The DVD navigator processes all keystroke information and sends new highlight information each time a button state changes.</span></span> <span data-ttu-id="4db5e-136">Die Informationen beschreiben jeweils nur einen Modus für eine Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="4db5e-136">The information describes only one mode of one button at a time.</span></span> <span data-ttu-id="4db5e-137">Sie enthält ein Anzeige Rechteck in Pixelkoordinaten des Bildschirms oder eine Anzeige des unter Bilds, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4db5e-137">It includes a display rectangle in pixel coordinates of the screen, or a display of the subpicture, if present.</span></span> <span data-ttu-id="4db5e-138">Die Struktur enthält auch Farb-und Kontrast Informationen, jedoch nur für den aktuellen Zustand der aktuell ausgewählten Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="4db5e-138">The structure also contains color and contrast information, but only for the present state of the currently selected button.</span></span> <span data-ttu-id="4db5e-139">Das Format wird in der DVD-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="4db5e-139">The format is defined in the DVD specification.</span></span>

<span data-ttu-id="4db5e-140">Die Hervorhebungs Informationen enthalten Zeitstempel für Start und Ende.</span><span class="sxs-lookup"><span data-stu-id="4db5e-140">Highlight information contains Start and End time stamps.</span></span> <span data-ttu-id="4db5e-141">Diese befinden sich in den gleichen Einheiten wie andere Zeitstempel, mit zwei Ausnahmen: ein Start Zeitstempel von 0xFFFFFFFF bedeutet, dass die Hervorhebungs Eigenschaft beim Empfang wirksam ist, und ein Endzeit Stempel von 0xFFFFFFFF bedeutet, dass die Hervorhebungs Eigenschaft gültig ist, bis die nächste Hervorhebung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="4db5e-141">These are in the same units as other time stamps, with two exceptions: A Start time stamp of 0xFFFFFFFF means the highlight property is effective upon receipt, and an End time stamp of 0xFFFFFFFF means the highlight property is valid until next highlight received.</span></span>

<span data-ttu-id="4db5e-142">Das hliss-Feld ist wie in der DVD-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="4db5e-142">The HLISS field is as defined in the DVD specification.</span></span> <span data-ttu-id="4db5e-143">Der Wert 0 (null) gibt an, dass alle Highlights ungültig sind und der Decoder alle Highlights deaktivieren soll.</span><span class="sxs-lookup"><span data-stu-id="4db5e-143">A value of zero indicates that all highlights are invalid and the decoder should disable all highlights.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db5e-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4db5e-144">Requirements</span></span>



| <span data-ttu-id="4db5e-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4db5e-145">Requirement</span></span> | <span data-ttu-id="4db5e-146">Wert</span><span class="sxs-lookup"><span data-stu-id="4db5e-146">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4db5e-147">Header</span><span class="sxs-lookup"><span data-stu-id="4db5e-147">Header</span></span><br/> | <dl> <span data-ttu-id="4db5e-148"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db5e-148"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db5e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4db5e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db5e-150">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="4db5e-150">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




