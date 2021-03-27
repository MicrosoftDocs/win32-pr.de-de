---
description: Windows GDI+ bietet verschiedene Qualitätsstufen zum Zeichnen von Text. In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität.
ms.assetid: 780d97ec-f446-4d19-837f-517a7d6dd27d
title: Antialiasing mit Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c7b7c59a436db6c16251aa8e866648eed5cc51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994462"
---
# <a name="antialiasing-with-text"></a>Antialiasing mit Text

Windows GDI+ bietet verschiedene Qualitätsstufen zum Zeichnen von Text. In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität.

Die Qualitätsstufe ist eine Eigenschaft der [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse. Um die Qualitätsstufe festzulegen, müssen Sie die [**Graphics:: settextrenderinghint**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) -Methode eines **Grafik** Objekts aufrufen. Die **Graphics:: settextrenderinghint** -Methode empfängt eines der Elemente der [**TextRenderingHint**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint) -Enumeration, die in "gdiplusenums. h" deklariert wird.

GDI+ bietet herkömmliches Antialiasing und eine neue Art von Antialiasing auf der Grundlage von Microsoft ClearType-Anzeige Technologie, die nur unter Windows XP und Windows Server 2003 und höheren Versionen von Windows verfügbar ist. ClearType Glättung verbessert die Lesbarkeit von Farb-LCD-Monitoren, die über eine digitale Schnittstelle verfügen, z. b. die Monitore in Laptops und hochwertige flatdesktopdisplays. Die Lesbarkeit von CRT-Bildschirmen wird ebenfalls verbessert.

ClearType ist von der Ausrichtung und Reihenfolge der LCD-Streifen abhängig. ClearType wird zurzeit nur für vertikale Streifen implementiert, die mit einer beliebigen Bestellung geordnet sind. Dies kann ein Problem sein, wenn Sie einen Tablet PC verwenden, bei dem die Anzeige in beliebiger Richtung ausgerichtet werden kann, oder wenn Sie einen Bildschirm verwenden, der von Querformat zu Hochformat geschaltet werden kann.

Im folgenden Beispiel wird Text mit zwei verschiedenen Qualitätseinstellungen gezeichnet:


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

![Screenshot einer Zeichenfolge, deren Zeichen verzweigte Ränder aufweisen, mit einem mit glatten Kanten](images/fontstext10.png)

 

 



