---
title: Histogrammeffekt
description: Verwenden Sie den Histogrammeffekt, um ein Histogramm für die Eingabebitmap basierend auf der angegebenen Anzahl von Bins zu generieren.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- Histogrammeffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08477a832b2dbf758d26a16e78905f8530d4d4525205cbc85e9d138f8b3bded7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044410"
---
# <a name="histogram-effect"></a>Histogrammeffekt

Verwenden Sie den Histogrammeffekt, um ein Histogramm für die Eingabebitmap basierend auf der angegebenen Anzahl von Bins zu generieren.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Histogram.

-   [Beispiel](#example)
-   [Effect-Eigenschaften](#effect-properties)
-   [Kanalauswahl](#channel-selectors)
-   [Datenausgabe](#data-output)
-   [Anmerkungen](#remarks)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example"></a>Beispiel



| Vorher                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| Graph der Histogrammausgabedaten                         |
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



## <a name="effect-properties"></a>Effect-Eigenschaften

Dies ist die Gleichung zum Generieren der Ausgabe.

![die Gleichung, um die Ausgabe des Histogrammeffekts zu generieren.](images/histogram-formula.png)

*i* wird von 0 bis zur Anzahl der Behälter ausgewertet. Der Effekt generiert ein Histogramm für Pixelwerte zwischen 0 und 1. Werte außerhalb dieses Bereichs werden an den Bereich geklammert. Der Bereich eines bestimmten Buckets hängt von der Anzahl der Buckets ab. Dieser Effekt funktioniert bei geraden Bitmappixeln. Die Farbkanäle der Eingabebitmap werden durch den Alphakanal geteilt, um diesen Effekt zu berechnen.



| Anzeigename und Indexenumeration                                             | Typ und Standardwert                                                   | BESCHREIBUNG                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> D2D1 \_ HISTOGRAM \_ PROP \_ NUM \_ BINS<br/>                 | UINT32<br/> 256<br/>                                         | Gibt die Anzahl der für das Histogramm verwendeten Bins an. Der Bereich der Intensitätswerte, die in einen bestimmten Bucket fallen, hängt von der Anzahl der angegebenen Buckets ab.                              |
| ChannelSelect<br/> D2D1 \_ HISTOGRAM \_ PROP \_ CHANNEL \_ SELECT<br/>     | \_D2D1-KANALAUSWAHL \_<br/> \_D2D1-KANALAUSWAHL \_ \_ R<br/> | Gibt den Kanal an, der zum Generieren des Histogramms verwendet wird. Dieser Effekt hat eine einzelne Datenausgabe, die dem angegebenen Kanal entspricht. Weitere [Informationen finden Sie unter](#channel-selectors) Kanalauswahl. |
| HistogramOutput<br/> D2D1 \_ HISTOGRAM \_ PROP \_ HISTOGRAM \_ OUTPUT<br/> | schweben\[\]<br/> Nur Ausgabeeigenschaft.<br/>                    | Das Ausgabearray.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Kanalauswahl



| Enumeration                | Beschreibung                                                           |
|----------------------------|-----------------------------------------------------------------------|
| \_D2D1-KANALAUSWAHL \_ \_ R | Der Effekt generiert die Histogrammausgabe basierend auf dem roten Kanal.   |
| \_D2D1-KANALAUSWAHL \_ \_ G | Der Effekt generiert die Histogrammausgabe basierend auf dem grünen Kanal. |
| \_D2D1-KANALAUSWAHL \_ \_ B | Der Effekt generiert die Histogrammausgabe basierend auf dem blauen Kanal.  |
| \_D2D1-KANALAUSWAHL \_ \_ A | Der Effekt generiert die Histogrammausgabe basierend auf dem Alphakanal. |



 

## <a name="data-output"></a>Datenausgabe

Dieser Effekt gibt eine FLOAT-Datei mit der Anzahl der Elemente aus, die \[ \] der Anzahl der angegebenen Bins entspricht. Jedes Element in FLOAT \[ \] ist ein float-Element. Der Wert des Elements entspricht der Anzahl der Elemente in diesem Bin.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die [**CreateEffect-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) schlägt fehl, wenn das Gerät DirectCompute nicht unterstützt und HRESULT = D2DERR \_ INSUFFICIENT DEVICE CAPABILITIES \_ \_ zurückgibt. Alle DirectX11-Karten und DirectX10-Karten, die DirectCompute unterstützen, können den Effekt verwenden.

 

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

 

