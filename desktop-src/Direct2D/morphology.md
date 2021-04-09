---
title: Morphologieeffekt
description: Verwenden Sie den morphologieeffekt, um die Randgrenzen eines Bilds dünn oder Thicken zu können.
ms.assetid: 4B3CFC51-D556-4729-B433-7307C80291F4
keywords:
- morphologieeffekte
- Dilate-Auswirkung
- Auswirkung Erodieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43cf41810ae0b16c9bc96dd37473a0231fc132c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104727"
---
# <a name="morphology-effect"></a>Morphologieeffekt

Verwenden Sie den morphologieeffekt, um die Randgrenzen eines Bilds dünn oder Thicken zu können. Dieser Effekt erstellt einen Kernel, der das 2fache der von Ihnen angegebenen Width-und Height-Werte ist. Dieser Effekt zentriert den Kernel auf dem Pixel, das er berechnet, und gibt den maximalen Wert im Kernel (bei der Vergrößerung) oder den minimalen Wert im Kernel (wenn das Eroding erfolgt) zurück.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Morphology.

## <a name="example-images"></a>Beispiel Bilder

Dieses Beispiel zeigt die Ausgabe der Auswirkung, wenn der eroeromodus verwendet wird.



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Nach                                                      |
| ![das Bild nach der Transformation.](images/7-morphology.png) |



 


```C++
ComPtr<ID2D1Effect> morphologyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Morphology, &morphologyEffect);

morphologyEffect->SetInput(0, bitmap);

morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_MODE, D2D1_MORPHOLOGY_MODE_ERODE);
morphologyEffect->SetValue(D2D1_MORPHOLOGY_PROP_WIDTH, 14);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(morphologyEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                          | Typ und Standardwert                                                     | BESCHREIBUNG                                                                                                                                                       |
|-------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> D2D1 \_ Morphology- \_ Prop- \_ Modus<br/>     | D2D1- \_ \_ morphologiemodus<br/> D2D1 \_ \_ morphologiemodus \_ Erodieren<br/> | Der morphologiemodus. Die verfügbaren Modi sind erodiert (Flatten) und Dilate (Thicken).<br/> Weitere Informationen finden Sie unter [morphologiemodi](#morphology-modes) .<br/> |
| Breite<br/> Breite der D2D1- \_ morphologiebreite \_ \_<br/>   | UINT<br/> 1<br/>                                               | Größe des Kernels in der X-Richtung. Die Einheiten befinden sich in Dips. Die Werte müssen zwischen 1 und 100 (einschließlich) liegen.                                                         |
| Höhe<br/> D2D1 \_ Morphology \_ Prop \_ Height<br/> | UINT<br/> 1<br/>                                               | Größe des Kernels in der Y-Richtung. Die Einheiten befinden sich in Dips. Die Werte müssen zwischen 1 und 100 (einschließlich) liegen.                                                         |



 

## <a name="morphology-modes"></a>Morphologiemodi



| Name                           | BESCHREIBUNG                                                    |
|--------------------------------|----------------------------------------------------------------|
| D2D1 \_ \_ morphologiemodus \_ Erodieren  | Der maximale Wert jedes RGB-Kanals im Kernel wird verwendet. |
| D2D1 \_ \_ morphologiemodus \_ Dilate | Der minimale Wert jedes RGB-Kanals im Kernel wird verwendet. |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Beim Dilate-Modus wächst die Größe der Ausgabe Bitmap: 

| Anforderung | Wert |
|--------------------------|-----------------------------------------|
| Ergebnis der Ausgabe Bitmap X = | INT (float (Width) \* ((Benutzer dpi)/96))  |
| Ergebnis der Ausgabe Bitmap Y = | INT (float (Height) \* ((Benutzer dpi)/96)) |



 

Für den eroeromodus verkleinert sich die Größe der Ausgabe Bitmap:

| Anforderung | Wert |
|--------------------------|------------------------------------------|
| Ergebnis der Ausgabe Bitmap X = | INT (float (-Width) \* ((Benutzer dpi)/96))  |
| Ergebnis der Ausgabe Bitmap Y = | INT (float (-Height) \* ((Benutzer dpi)/96)) |



 

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

 

