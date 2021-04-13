---
title: Histogrammeffekt
description: Verwenden Sie den histogrammeffekt, um ein Histogramm für die Eingabe Bitmap basierend auf der angegebenen Anzahl von Containern zu generieren.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- histogrammeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391829"
---
# <a name="histogram-effect"></a>Histogrammeffekt

Verwenden Sie den histogrammeffekt, um ein Histogramm für die Eingabe Bitmap basierend auf der angegebenen Anzahl von Containern zu generieren.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Histogram.

-   [Beispiel](#example)
-   [Effekt Eigenschaften](#effect-properties)
-   [Kanalselektoren](#channel-selectors)
-   [Datenausgabe](#data-output)
-   [Anmerkungen](#remarks)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example"></a>Beispiel



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Diagramm der histogrammausgabedaten                         |
| ![das Bild nach der Transformation.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a>Effekt Eigenschaften

Hier ist die Gleichung, um die Ausgabe zu generieren.

![die Gleichung, die die Ausgabe des histogrammeffekts generieren soll.](images/histogram-formula.png)

*ich* werde zwischen 0 und der Anzahl der Behälter ausgewertet. Der Effekt generiert ein Histogramm für Pixelwerte zwischen 0 und 1. Werte, die außerhalb dieses Bereichs liegen, werden an den Bereich gebunden. Der Bereich eines bestimmten Bucket hängt von der Anzahl der Eimer ab. Dieser Effekt funktioniert bei geraden Bitmap-Pixeln. Die Farbkanäle der Eingabe Bitmap werden durch den Alphakanal dividiert, um diesen Effekt zu berechnen.



| Anzeige Name und indexenumeration                                             | Typ und Standardwert                                                   | BESCHREIBUNG                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Numbins<br/> D2D1 \_ Histogram \_ Prop \_ NUM- \_ Behälter<br/>                 | UINT32<br/> 256<br/>                                         | Gibt die Anzahl der für das Histogramm verwendeten Container an. Der Bereich der Intensitätswerte, die in einem bestimmten Bucket liegen, hängt von der Anzahl der angegebenen Bucket ab.                              |
| Channelselect<br/> D2D1 \_ Histogramm- \_ Prop- \_ Kanal \_ auswählen<br/>     | D2D1 \_ - \_ kanalselektor<br/> D2D1 \_ - \_ kanalselektor \_ R<br/> | Gibt den Kanal an, der zum Generieren des Histogramms verwendet wird. Dieser Effekt hat eine einzelne Datenausgabe, die dem angegebenen Kanal entspricht. Weitere Informationen finden Sie unter [kanalselektoren](#channel-selectors) . |
| Histogrammausgabe<br/> D2D1 \_ Histogramm \_ - \_ \_ Compilerausgabe<br/> | Hafen\[\]<br/> Nur Ausgabe Eigenschaft.<br/>                    | Das Ausgabe Array.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Kanalselektoren



| Enumeration                | Beschreibung                                                           |
|----------------------------|-----------------------------------------------------------------------|
| D2D1 \_ - \_ kanalselektor \_ R | Der Effekt generiert die histogrammausgabe basierend auf dem roten Kanal.   |
| D2D1 \_ Kanal \_ Auswahl \_ G | Der Effekt generiert die histogrammausgabe basierend auf dem grünen Kanal. |
| D2D1 \_ - \_ kanalselektor \_ B | Der Effekt generiert die histogrammausgabe basierend auf dem blauen Kanal.  |
| D2D1 \_ \_ kanalselektor \_ A | Der Effekt generiert die histogrammausgabe basierend auf dem Alphakanal. |



 

## <a name="data-output"></a>Datenausgabe

Dieser Effekt gibt einen float-Wert \[ \] mit der Anzahl der Elemente aus, die der Anzahl der angegebenen Behälter entspricht. Jedes Element in der Gleit Komma Zahl \[ \] ist ein float-Wert. Der Wert des-Elements entspricht der Anzahl der Elemente in diesem bin.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Methode " [**deateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) " schlägt fehl, wenn das Gerät DirectCompute nicht unterstützt und HRESULT = D2DERR \_ unzureichende \_ Gerätefunktionen zurückgibt \_ . Alle DirectX11 Cards und DirectX10-Karten, die DirectCompute unterstützen, können den Effekt nutzen.

 

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

 

