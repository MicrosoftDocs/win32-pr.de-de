---
title: Atlas-Effekt
description: Sie können diesen Effekt verwenden, um einen Teil eines Images ausausgaben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b0d55e7751ef73d8f6bdff65a6ae5d5933695600a1003b9c4a010231628019
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929049"
---
# <a name="atlas-effect"></a>Atlas-Effekt

Sie können diesen Effekt verwenden, um einen Teil eines Images ausausgaben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Atlas.

Der Atlaseffekt ist nützlich, wenn Sie ein großes Bild laden möchten, das aus vielen kleineren Bildern besteht, z. B. verschiedenen Frames eines Sprite.

So erstellen Sie die Ausgabe des Effekts:

1.  Endt die Eingabe in die *gegebene InputRect-Eigenschaft.*
2.  Übersetzt den Ursprung des Ergebnisses in (0,0).

> [!Note]  
> Die *InputPaddingRect-Eigenschaft* sollte nur dann größer sein, wenn die Pixel zwischen den beiden Rechtecke in der Eingabe transparent schwarz sind. Dies kann dazu führen, dass Direct2D den Graphen optimaler ausführen kann.

 

Hier ist ein Beispiel für den Effekt. Dieses Bild ist zu Veranschaulichungszwecken klein und einfach.

![Eingabebild.](images/atlas.png)

Das obige Bild ist die Eingabe für den Effekt. Der Code hier erstellt einen Atlaseffekt, legt die Eingabe fest, legt das Eingaberechteck fest und zeichnet dann die Ausgabe.


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



Der vorangehende Code wählt ein Rechteck aus, das sich um das zweite Dreieck befindet. Die Padding um sie wird ignoriert. Hier sehen Sie das resultierende Bild.

![Ausgabebild.](images/atlas2.png)

> [!Note]  
> Dies ist eine Situation, in der Sie ein *InputPaddingRect* angeben können, da die Auf padding transparent schwarz ist. Das Rechteck wäre `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                             | BESCHREIBUNG                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ RECT<br/>                 | Der Teil des Bilds, der an den nächsten Effekt übergeben wird.<br/> Typ: D2D1 \_ VECTOR \_ 4F<br/> Der Standardwert ist (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX). <br/> |
| InputPaddingRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ PADDING \_ RECT<br/> | Die maximale Größe, die für das Ausgaberechteck entnommen wurde.<br/> Typ: D2D1 \_ VECTOR \_ 4F<br/> Der Standardwert ist (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX).<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

