---
title: Atlas-Effekt
description: Sie können diesen Effekt verwenden, um einen Teil eines Bilds auszugeben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478234"
---
# <a name="atlas-effect"></a>Atlas-Effekt

Sie können diesen Effekt verwenden, um einen Teil eines Bilds auszugeben, aber den Bereich außerhalb des Teils für die Verwendung in nachfolgenden Vorgängen beibehalten.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Atlas.

Der Atlas-Effekt ist hilfreich, wenn Sie ein umfangreiches Bild laden möchten, das aus vielen kleineren Bildern besteht, z. b. aus verschiedenen Rahmen eines Sprite.

So erstellen Sie die Ausgabe:

1.  Fügt die Eingabe in die angegebene *inputrect* -Eigenschaft ein.
2.  Übersetzt den Ursprung des Ergebnisses in (0,0).

> [!Note]  
> Die *inputpaddingrect* -Eigenschaft sollte nur dann größer sein, wenn die Pixel zwischen den zwei Rechtecke in der Eingabe transparent sind. Dies kann dazu führen, dass Direct2D das Diagramm optimaler ausführt.

 

Im folgenden finden Sie ein Beispiel für den Effekt. Dieses Bild ist für Illustrationszwecke klein und einfach.

![Eingabebild.](images/atlas.png)

Die vorherige Abbildung ist die Eingabe für den Effekt. Der Code hier erstellt einen Atlas-Effekt, legt die Eingabe fest, legt das Eingabe Rechteck fest und zeichnet dann die Ausgabe.


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



Der vorangehende Code wählt ein Rechteck aus, das sich um das zweite Dreieck dreht. Der Abstand um diese wird ignoriert. Hier sehen Sie das resultierende Image.

![Ausgabe Bild.](images/atlas2.png)

> [!Note]  
> Dies ist eine Situation, in der Sie ggf. eine *inputpaddingrect* -Angabe festlegen können, da der Abstand transparent schwarz ist. Das Rechteck wäre `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                             | BESCHREIBUNG                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Input Rect<br/> D2D1 \_ Atlas \_ - \_ Eingabe \_ Rect<br/>                 | Der Teil des Bilds, der an den nächsten Effekt weitergeleitet wird.<br/> Typ: D2D1 \_ Vector \_ 4f<br/> Der Standardwert ist (-f \_ Max,-f Max \_ , SLT \_ Max, SLT \_ max). <br/> |
| Input paddingrect<br/> D2D1 \_ Atlas \_ \_ Eingabe \_ \_ Auffüll Auffüll Text Rect<br/> | Die maximale Größe, die für das Ausgabe Rechteck Stichprobe ist.<br/> Typ: D2D1 \_ Vector \_ 4f<br/> Der Standardwert ist (-f \_ Max,-f Max \_ , SLT \_ Max, SLT \_ max).<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

