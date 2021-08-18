---
title: Anpassen von Menübandfarben
description: Das Windows Menübandframework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Menüband-Benutzeroberflächenelemente zur Laufzeit anzupassen.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows Menüband, Anpassen von Farben
- Menüband, Anpassen von Farben
- Anpassen von Windows Menübandfarben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef83c40d49656c82aabfbf41c4ec5375f7f3f54f063ccf30d917e740f87408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710890"
---
# <a name="customizing-ribbon-colors"></a>Anpassen von Menübandfarben

Das Windows Menübandframework macht eine Reihe von Farbeigenschaften verfügbar, die es einer Anwendung ermöglichen, die Darstellung verschiedener Menüband-Benutzeroberflächenelemente zur Laufzeit anzupassen.

-   [Introduction (Einführung)](#introduction)
-   [Angeben von Menübandfarben](#specify-ribbon-colors)
-   [Konvertieren von RGB in HSB](#convert-rgb-to-hsb)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Die [in der folgenden Tabelle](windowsribbon-reference-properties-framework.md) aufgeführten Framework-Eigenschaftsschlüssel werden verwendet, um die Farbe verschiedener Benutzeroberflächenelemente in einer Menübandanwendung fest zu legen. Diese Eigenschaften ermöglichen es dem Menübandframework, Personalisierung, Identitätsanforderungen und Brandingspezifikationen anwendungsübergreifend zu unterstützen.

| Menübandfarbe                     | Framework-Eigenschaftsschlüssel                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hintergrundfarbe                 | [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Hervorhebungsfarbe (nur Windows 7) | [Benutzeroberfläche \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)**Eingeführt in Windows 8**: ** [Ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Textfarbe                       | [Benutzeroberfläche \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)–Eingeführt in Windows 8 **:** Änderungen am Standardwert von [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 erfordern möglicherweise eine Anpassung der [ \_ Benutzeroberfläche PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Menüband-Apps, die für Windows 7 entwickelt wurden.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Angeben von Menübandfarben

Das Menübandframework verwendet ein Farbmodell für Farbton, Sättigung, Helligkeit (HSB), das sich von den gängigeren Farbräumen für Farbton, Sättigung, Helligkeit (HSL) oder Farbton, Sättigung, Wert (HSV) unterscheidet. B stellt insbesondere eine gesamter Helligkeits- oder Helligkeitsstufe dar, anstatt die Helligkeit einer bestimmten Farbe.

Um die Farbe von Benutzeroberflächenelementen im Menübandframework anzugeben, weist eine Anwendung jeder der globalen Farbeigenschaften HSB-Werte zu. Diese Werte werden dann universell auf alle Menübandelemente angewendet, wie dies für die Menübandanwendung erforderlich ist (das Framework unterstützt das Zuweisen von HSB-Werten zu einzelnen Elementen und Steuerelementen nicht).

Eingeführt in Windows 8**: **[Ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

In der folgenden Tabelle werden die HSB-Parameter des Menübandframework beschrieben.



Komponente

Beschreibung

Angepasste Werte\*

Hue (H)

Die Tatsächliche Farbe wird in der Regel als Wert aus einem ringförmigen Bereich von 0 bis 359 Grad identifiziert.

0 (rot) bis 255 (rot)

Sättigung (S)

Die Bzw. die Sättigung der Farbe, gemessen als Prozentsatz von 0 bis 100 %.

0 (grau) bis 255 (vollständig ausgesättigt)

Helligkeit (B)

Die Gesamtstärke oder Die Helligkeit der Farbe, gemessen als Prozentsatz von 0 bis 100 %.

0 (dunkel) bis 255 (hell)

\* Der ursprüngliche Bereich für jeden Parameterwert wird für das Framework in einen Bereich von 0 bis 255 übersetzt.



 

HSB-Werte identifizieren keine bestimmten Farben. Stattdessen beeinflusst die Kombination von HSB-Eigenschaftswerten, wie Farbverläufe in der gesamten Benutzeroberfläche relativ zueinander angepasst werden.

Beim Zuweisen benutzerdefinierter HSB-Werte zu [ \_ UI PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) und [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)wird empfohlen, dass diese Werte einen ausreichend hohen Kontrast haben, um die Lesbarkeit sicherzustellen. Insbesondere sollte die Textfarbe dunkler als der hellste Schattierung der Menübandbenutzeroberfläche sein. Bei Bedarf passt das Framework den \_ PKEY GlobalTextColor HSB-Wert der Benutzeroberfläche automatisch an, um ausreichend Kontrast zu jedem Hintergrundton oder Farbverlauf zu bieten, der von \_ \_ PKEY GlobalBackgroundColor der Benutzeroberfläche abgeleitet \_ ist.

> [!Note]  
> In Windows 7 kann [ \_ ui PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) unabhängig von [ \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)der Benutzeroberfläche festgelegt werden.

 

Im folgenden Beispiel wird veranschaulicht, wie sie eine benutzerdefinierte Farbe für die Eigenschaften [ \_ PKEY \_ GlobalTextColor,](windowsribbon-reference-properties-uipkey-globaltextcolor.md) [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)und [UI \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) angeben.


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

In diesem Abschnitt wird die Formel beschrieben, die erforderlich ist, um einen HSB-Wert des Menübandframework, in diesem Beispiel die [ \_ Ui PKEY \_ GlobalBackgroundColor,](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) dynamisch mit einer bestimmten RGB-Farbe zur Laufzeit zu abgleichen.

Der Hintergrund der Registerkartenzeile wird als Bezugspunkt verwendet, da er im Vergleich zum Helligkeitsverlauf des Menübandhintergrunds als flache Farboberfläche gerendert wird.

Eine vorläufige Konvertierung ist erforderlich, um einen HSL-Zwischenwert zu erhalten. Dieser HSL-Wert kann dann in einen HSB-Wert konvertiert werden.

> [!Note]  
> Die Konvertierung von RGB in HSL lässt sich mit den meisten Fotobearbeitungssoftware problemlos erreichen.

 

Die Konvertierung von HSL (mit jeder Komponente im Bereich von 0,0 bis 1,0) in eine Menüband-HSB-Einstellung wird mithilfe der folgenden Formeln durchgeführt:

-   H<sub>background</sub> = Round(255.0 H)
-   S<sub>background</sub> = Round(255.0 S)
-   B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Farbrichtlinien](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Frameworkeigenschaften](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





