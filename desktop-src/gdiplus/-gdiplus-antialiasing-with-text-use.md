---
description: Windows GDI+ bietet verschiedene Qualitätsstufen für das Zeichnen von Text. In der Regel dauert das Rendern mit höherer Qualität mehr Verarbeitungszeit als rendern mit geringerer Qualität.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Antialiasing mit Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9411206351340f58b63196ff880745743ad92325918b112ad2ddb5bcb8591e9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249924"
---
# <a name="antialiasing-with-text"></a>Antialiasing mit Text

Windows GDI+ bietet verschiedene Qualitätsstufen für das Zeichnen von Text. In der Regel dauert das Rendern mit höherer Qualität mehr Verarbeitungszeit als rendern mit geringerer Qualität.

Die Qualitätsstufe ist eine Eigenschaft der [**Graphics-Klasse.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Um die Qualitätsstufe festzulegen, rufen Sie die [**Graphics::SetTextRenderingHint-Methode**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) eines **Graphics-Objekts** auf. Die **Graphics::SetTextRenderingHint-Methode empfängt** eines der Elemente der [**TextRenderingHint-Enumeration,**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) die in Gdiplusenums.h deklariert ist.

GDI+ bietet herkömmliches Antialiasing und eine neue Art von Antialiasing basierend auf der Microsoft ClearType-Anzeigetechnologie, die nur auf Windows XP und Windows Server 2003 und höher von Windows verfügbar ist. Die ClearType-Glättung verbessert die Lesbarkeit von COLOR-Monitoren, die über eine digitale Schnittstelle verfügen, z. B. die Monitore in Laptops und hochwertige flache Desktopanzeigen. Die Lesbarkeit auf CRT-Bildschirmen wurde ebenfalls etwas verbessert.

ClearType ist abhängig von der Ausrichtung und Reihenfolge der STRIP-Stripes. Derzeit ist ClearType nur für vertikale Stripes implementiert, die rgb geordnet sind. Dies kann ein Problem sein, wenn Sie einen Tablet-PC verwenden, auf dem die Anzeige in beliebiger Richtung ausgerichtet werden kann, oder wenn Sie einen Bildschirm verwenden, der von querformatiert in hochformatiert werden kann.

Im folgenden Beispiel wird Text mit zwei verschiedenen Qualitätseinstellungen zeichnet:


```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 32, FontStyleRegular, UnitPixel);
SolidBrush  solidBrush(Color(255, 0, 0, 255));
WCHAR       string1[] = L"SingleBitPerPixel";
WCHAR       string2[] = L"AntiAlias";

graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);
graphics.DrawString(string1, -1, &font, PointF(10.0f, 10.0f), &solidBrush);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
graphics.DrawString(string2, -1, &font, PointF(10.0f, 60.0f), &solidBrush);
            
```



Die folgende Abbildung zeigt die Ausgabe des vorangehenden Codes.

![Screenshot einer Zeichenfolge, deren Zeichen verzweigte Kanten aufweisen, gegenüber einer Zeichenfolge mit geglätteten Rändern](images/fontstext10.png)

 

 



