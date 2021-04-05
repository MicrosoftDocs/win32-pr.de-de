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
# <a name="customizing-ribbon-colors"></a>Anpassen von Menü Band Farben

Das Windows-Menüband-Framework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Elemente der Multifunktionsleisten-Benutzeroberfläche zur Laufzeit anzupassen.

-   [Introduction (Einführung)](#introduction)
-   [Menü Band Farben angeben](#specify-ribbon-colors)
-   [Konvertieren von RGB in HSB](#convert-rgb-to-hsb)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Die in der folgenden Tabelle aufgeführten [Frameworks-Eigenschaften Schlüssel](windowsribbon-reference-properties-framework.md) werden verwendet, um die Farbe verschiedener Benutzeroberflächen Elemente in einer Menü Bandanwendung festzulegen. Diese Eigenschaften ermöglichen es dem Menüband-Framework, die Personalisierungs-, Identitäts-und brandingspezifikationen Anwendungs übergreifend zu unterstützen.

| Menüband-Farbe                     | Framework-Eigenschaften Schlüssel                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hintergrundfarbe                 | [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Hervorhebungs Farbe (nur Windows 7) | [Benutzeroberfläche \_ Pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* * * * eingeführt in Windows 8 * *: * * [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) kann nicht unabhängig von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)festgelegt werden.<br/> <br/>                                                              |
| Textfarbe                       | [Benutzeroberfläche \_ Pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * eingeführt in Windows 8 **:** Änderungen am Standardwert von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 erfordern möglicherweise eine Anpassung an [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Menüband-apps, die für Windows 7 entworfen wurden.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Menü Band Farben angeben

Das Menüband-Framework verwendet ein HSB-Farbmodell (Hue, Sättigung, Helligkeit), das sich von den Farbräumen der gängigeren Farbton, Sättigung, Leuchtkraft (HSL) oder Hue, Sättigung, Wert (HSV) unterscheidet. Insbesondere stellt B eine allgemeine Helligkeit oder eine Helligkeit dar, nicht die Helligkeit einer bestimmten Farbe.

Um die Farbe der Benutzeroberflächen Elemente im Menüband-Framework anzugeben, weist eine Anwendung den einzelnen globalen Farbeigenschaften HSB-Werte zu. Diese Werte werden dann universell auf alle Menü Band Elemente angewendet, wie dies für die Multifunktionsleistenanwendung erforderlich ist (das Zuweisen von HSB-Werten zu einzelnen Elementen und Steuerelementen wird vom Framework nicht unterstützt).

Eingeführt in Windows 8 * *: * *[UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) erhält denselben Wert wie [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

In der folgenden Tabelle werden die HSB-Parameter für das Menüband Framework beschrieben



Komponente

BESCHREIBUNG

Angepasste Werte\*

Farbton (H)

Die Farbe für das Pigment oder die tatsächliche Farbe wird in der Regel als Wert von einem zirkulär Bereich von 0 bis 359 Grad identifiziert.

0 (rot) bis 255 (rot)

Sättigung (en)

Die Reinheit oder Sättigung der Farbe, gemessen als Prozentsatz zwischen 0 und 100%.

0 (grau) bis 255 (vollständig ausgelastet)

Helligkeit (B)

Die Gesamthelligkeit oder Dunkelheit der Farbe, gemessen als Prozentsatz zwischen 0 und 100%.

0 (dunkel) bis 255 (hell)

\* Der ursprüngliche Bereich für jeden Parameterwert wird in einen Bereich von 0 bis 255 für das Framework übersetzt.



 

HSB-Werte identifizieren keine bestimmten Farben. Stattdessen wirkt sich die Kombination von HSB-Eigenschafts Werten darauf aus, wie Farbverläufe in der gesamten Benutzeroberfläche relativ zueinander angepasst werden.

Beim Zuweisen von benutzerdefinierten HSB-Werten zu [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) und [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)wird empfohlen, dass diese Werte einen hohen Kontrast aufweisen, um die Lesbarkeit zu gewährleisten. Die Textfarbe sollte vor allem dunkler sein als der leichtesten Farbton der Menüband-Benutzeroberfläche. Bei Bedarf passt das Framework den Benutzeroberflächen- \_ pkey \_ Global TextColor-HSB-Wert automatisch an, um einen ausreichenden Kontrast gegen alle Hintergrund Schattierungen oder Farbverläufe zu bieten, die von UI \_ pkey \_ globalbackgroundcolor abgeleitet werden.

> [!Note]  
> In Windows 7 kann [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) unabhängig von [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)festgelegt werden.

 

Im folgenden Beispiel wird veranschaulicht, wie eine benutzerdefinierte Farbe für die Eigenschaften " [UI \_ pkey \_ globaltextcolor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)", " [UI \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)" und " [UI \_ pkey \_ globalhighlightcolor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) " angegeben wird.


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



## <a name="convert-rgb-to-hsb"></a>Konvertieren von RGB in HSB

In diesem Abschnitt wird die Formel beschrieben, die für die dynamische Übereinstimmung eines HSB-Werts für den Menüband-Framework, die [Benutzeroberfläche \_ pkey \_ globalbackgroundcolor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in diesem Beispiel, für eine bestimmte RGB-Farbe zur Laufzeit erforderlich ist.

Der Hintergrund der Registerkarten Zeile wird als Bezugspunkt verwendet, da er im Vergleich zum Helligkeits Farbverlauf des Menüband-Hintergrunds als flache Farbfläche gerendert wird.

Zum Abrufen eines zwischen-HSL-Werts ist eine vorläufige Konvertierung erforderlich. Dieser HSL-Wert kann dann in einen HSB-Wert konvertiert werden.

> [!Note]  
> Die Konvertierung von RGB in HSL kann mit der meisten Fotobearbeitungssoftware problemlos durchgeführt werden.

 

Die Konvertierung von HSL (mit jeder Komponente im Bereich von 0,0 bis 1,0) in eine Menüband-HSB-Einstellung wird durch die folgenden Formeln erreicht:

-   H<sub>Background</sub> = Round (255.0 h)
-   S<sub>Background</sub> = Round (255.0 s)
-   B<sub>Background</sub> = Round (257.7 + 149,9 ln (L)), wenn 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farb Richtlinien](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Framework-Eigenschaften](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





