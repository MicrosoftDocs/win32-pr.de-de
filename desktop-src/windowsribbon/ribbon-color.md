---
title: Anpassen von Menü Band Farben
description: Das Windows-Menüband-Framework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Elemente der Multifunktionsleisten-Benutzeroberfläche zur Laufzeit anzupassen.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows-Menüband, Anpassen von Farben
- Multifunktionsleiste, Anpassen von Farben
- Anpassen von Windows-Menü Band Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723821"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="0a826-106">Anpassen von Menü Band Farben</span><span class="sxs-lookup"><span data-stu-id="0a826-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="0a826-107">Das Windows-Menüband-Framework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Elemente der Multifunktionsleisten-Benutzeroberfläche zur Laufzeit anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0a826-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="0a826-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="0a826-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0a826-109">Menü Band Farben angeben</span><span class="sxs-lookup"><span data-stu-id="0a826-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="0a826-110">Konvertieren von RGB in HSB</span><span class="sxs-lookup"><span data-stu-id="0a826-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="0a826-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a826-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0a826-112">Einführung</span><span class="sxs-lookup"><span data-stu-id="0a826-112">Introduction</span></span>

<span data-ttu-id="0a826-113">Die in der folgenden Tabelle aufgeführten [Frameworks-Eigenschaften Schlüssel](windowsribbon-reference-properties-framework.md) werden verwendet, um die Farbe verschiedener Benutzeroberflächen Elemente in einer Menü Bandanwendung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0a826-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="0a826-114">Diese Eigenschaften ermöglichen es dem Menüband-Framework, die Personalisierungs-, Identitäts-und brandingspezifikationen Anwendungs übergreifend zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0a826-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="0a826-115">Menüband-Farbe</span><span class="sxs-lookup"><span data-stu-id="0a826-115">Ribbon Color</span></span>                     | <span data-ttu-id="0a826-116">Framework-Eigenschaften Schlüssel</span><span class="sxs-lookup"><span data-stu-id="0a826-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a826-117">Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="0a826-117">Background color</span></span>                 | [<span data-ttu-id="0a826-118">UI \_ pkey \_ globalbackgroundcolor</span><span class="sxs-lookup"><span data-stu-id="0a826-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0a826-119">Hervorhebungs Farbe (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="0a826-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="0a826-120">[Benutzeroberfläche \_ Pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \* \* \* eingeführt in Windows 8 \* \*: \* \* [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) kann nicht unabhängig von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="0a826-121">Textfarbe</span><span class="sxs-lookup"><span data-stu-id="0a826-121">Text color</span></span>                       | <span data-ttu-id="0a826-122">[Benutzeroberfläche \_ Pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* eingeführt in Windows 8 **:** Änderungen am Standardwert von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 erfordern möglicherweise eine Anpassung an [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Menüband-apps, die für Windows 7 entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="0a826-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="0a826-123">Menü Band Farben angeben</span><span class="sxs-lookup"><span data-stu-id="0a826-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="0a826-124">Das Menüband-Framework verwendet ein HSB-Farbmodell (Hue, Sättigung, Helligkeit), das sich von den Farbräumen der gängigeren Farbton, Sättigung, Leuchtkraft (HSL) oder Hue, Sättigung, Wert (HSV) unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="0a826-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="0a826-125">Insbesondere stellt B eine allgemeine Helligkeit oder eine Helligkeit dar, nicht die Helligkeit einer bestimmten Farbe.</span><span class="sxs-lookup"><span data-stu-id="0a826-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="0a826-126">Um die Farbe der Benutzeroberflächen Elemente im Menüband-Framework anzugeben, weist eine Anwendung den einzelnen globalen Farbeigenschaften HSB-Werte zu.</span><span class="sxs-lookup"><span data-stu-id="0a826-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="0a826-127">Diese Werte werden dann universell auf alle Menü Band Elemente angewendet, wie dies für die Multifunktionsleistenanwendung erforderlich ist (das Zuweisen von HSB-Werten zu einzelnen Elementen und Steuerelementen wird vom Framework nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="0a826-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="0a826-128">Eingeführt in Windows 8 \* \*: \* \*[UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) erhält denselben Wert wie [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="0a826-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="0a826-129">In der folgenden Tabelle werden die HSB-Parameter für das Menüband Framework beschrieben</span><span class="sxs-lookup"><span data-stu-id="0a826-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="0a826-130">Komponente</span><span class="sxs-lookup"><span data-stu-id="0a826-130">Component</span></span>

<span data-ttu-id="0a826-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a826-131">Description</span></span>

<span data-ttu-id="0a826-132">Angepasste Werte\*</span><span class="sxs-lookup"><span data-stu-id="0a826-132">Adjusted Values\*</span></span>

<span data-ttu-id="0a826-133">Farbton (H)</span><span class="sxs-lookup"><span data-stu-id="0a826-133">Hue (H)</span></span>

<span data-ttu-id="0a826-134">Die Farbe für das Pigment oder die tatsächliche Farbe wird in der Regel als Wert von einem zirkulär Bereich von 0 bis 359 Grad identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a826-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="0a826-135">0 (rot) bis 255 (rot)</span><span class="sxs-lookup"><span data-stu-id="0a826-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="0a826-136">Sättigung (en)</span><span class="sxs-lookup"><span data-stu-id="0a826-136">Saturation (S)</span></span>

<span data-ttu-id="0a826-137">Die Reinheit oder Sättigung der Farbe, gemessen als Prozentsatz zwischen 0 und 100%.</span><span class="sxs-lookup"><span data-stu-id="0a826-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="0a826-138">0 (grau) bis 255 (vollständig ausgelastet)</span><span class="sxs-lookup"><span data-stu-id="0a826-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="0a826-139">Helligkeit (B)</span><span class="sxs-lookup"><span data-stu-id="0a826-139">Brightness (B)</span></span>

<span data-ttu-id="0a826-140">Die Gesamthelligkeit oder Dunkelheit der Farbe, gemessen als Prozentsatz zwischen 0 und 100%.</span><span class="sxs-lookup"><span data-stu-id="0a826-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="0a826-141">0 (dunkel) bis 255 (hell)</span><span class="sxs-lookup"><span data-stu-id="0a826-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="0a826-142">\* Der ursprüngliche Bereich für jeden Parameterwert wird in einen Bereich von 0 bis 255 für das Framework übersetzt.</span><span class="sxs-lookup"><span data-stu-id="0a826-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="0a826-143">HSB-Werte identifizieren keine bestimmten Farben.</span><span class="sxs-lookup"><span data-stu-id="0a826-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="0a826-144">Stattdessen wirkt sich die Kombination von HSB-Eigenschafts Werten darauf aus, wie Farbverläufe in der gesamten Benutzeroberfläche relativ zueinander angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="0a826-145">Beim Zuweisen von benutzerdefinierten HSB-Werten zu [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) und [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)wird empfohlen, dass diese Werte einen hohen Kontrast aufweisen, um die Lesbarkeit zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="0a826-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="0a826-146">Die Textfarbe sollte vor allem dunkler sein als der leichtesten Farbton der Menüband-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="0a826-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="0a826-147">Bei Bedarf passt das Framework den Benutzeroberflächen- \_ pkey \_ Global TextColor-HSB-Wert automatisch an, um einen ausreichenden Kontrast gegen alle Hintergrund Schattierungen oder Farbverläufe zu bieten, die von UI \_ pkey \_ globalbackgroundcolor abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="0a826-148">In Windows 7 kann [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) unabhängig von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="0a826-149">Im folgenden Beispiel wird veranschaulicht, wie eine benutzerdefinierte Farbe für die Eigenschaften " [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)", " [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)" und " [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0a826-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="0a826-150">Konvertieren von RGB in HSB</span><span class="sxs-lookup"><span data-stu-id="0a826-150">Convert RGB to HSB</span></span>

<span data-ttu-id="0a826-151">In diesem Abschnitt wird die Formel beschrieben, die für die dynamische Übereinstimmung eines HSB-Werts für den Menüband-Framework, die [Benutzeroberfläche \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in diesem Beispiel, für eine bestimmte RGB-Farbe zur Laufzeit erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0a826-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="0a826-152">Der Hintergrund der Registerkarten Zeile wird als Bezugspunkt verwendet, da er im Vergleich zum Helligkeits Farbverlauf des Menüband-Hintergrunds als flache Farbfläche gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0a826-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="0a826-153">Zum Abrufen eines zwischen-HSL-Werts ist eine vorläufige Konvertierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0a826-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="0a826-154">Dieser HSL-Wert kann dann in einen HSB-Wert konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="0a826-155">Die Konvertierung von RGB in HSL kann mit der meisten Fotobearbeitungssoftware problemlos durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0a826-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="0a826-156">Die Konvertierung von HSL (mit jeder Komponente im Bereich von 0,0 bis 1,0) in eine Menüband-HSB-Einstellung wird durch die folgenden Formeln erreicht:</span><span class="sxs-lookup"><span data-stu-id="0a826-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="0a826-157">H<sub>Background</sub> = Round (255.0 h)</span><span class="sxs-lookup"><span data-stu-id="0a826-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="0a826-158">S<sub>Background</sub> = Round (255.0 s)</span><span class="sxs-lookup"><span data-stu-id="0a826-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="0a826-159">B<sub>Background</sub> = Round (257.7 + 149,9 ln (L)), wenn 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="0a826-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a826-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0a826-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a826-161">Farb Richtlinien</span><span class="sxs-lookup"><span data-stu-id="0a826-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="0a826-162">Framework-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0a826-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





