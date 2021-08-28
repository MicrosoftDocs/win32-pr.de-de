---
description: Festlegen von Medientypen für DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Festlegen von Medientypen für DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fd437ae54d2e5baec35eb415dd8d04e4d3a3fe5992b8ba73f6d25c77f0475a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904250"
---
# <a name="setting-media-types-on-a-dmo"></a>Festlegen von Medientypen für DMO

Bevor ein DMO Daten verarbeiten kann, muss der Client den Medientyp für jeden Stream festlegen. (Es gibt eine geringfügige Ausnahme von dieser Regel. Weitere Informationen finden Sie unter [Optionale Streams](optional-streams.md).) Um die Anzahl der Streams zu finden, rufen Sie die [**IMediaObject::GetStreamCount-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) auf:


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Diese Methode gibt zwei Werte zurück: die Anzahl der Eingaben und die Anzahl der Ausgaben. Diese Werte werden für die Lebensdauer des DMO.

**Bevorzugte Typen**

Für jeden Stream weist DMO eine Liste möglicher Medientypen in der bevorzugten Reihenfolge zu. Die bevorzugten Typen können beispielsweise 32-RGB, 24-Bit RGB und 16-Bit RGB in dieser Reihenfolge sein. Wenn der Client die Medientypen fest legt, kann er diese Listen als Hinweis verwenden. Um einen bevorzugten Typ für einen Stream abzurufen, rufen Sie die [**IMediaObject::GetInputType-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) oder [**die IMediaObject::GetOutputType-Methode**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) auf. Geben Sie die Streamnummer und einen Indexwert für den Typ an (beginnend bei null). Der folgende Code ruft beispielsweise den ersten bevorzugten Typ aus dem ersten Eingabestream ab:


```C++
DMO_MEDIA_TYPE mt
hr = pDMO->GetInputType(0, 0, &mt)
if (SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
}
```



Um alle bevorzugten Medientypen in einem bestimmten Stream aufzählen zu können, verwenden Sie eine Schleife, die den Typindex inkrementiert, bis die Methode DMO E NO MORE ITEMS zurückgibt, wie im folgenden Beispiel \_ \_ \_ \_ gezeigt:


```C++
DMO_MEDIA_TYPE mt;
DWORD dwType = 0;
while (hr = pDMO->GetInputType(0, dwType, &mt), SUCCEEDED(hr))
{
    // Examine this media type (not shown).
    /* ... */

    // Free the format block.
    MoFreeMediaType(&mt);
    ++dwType;
}
```



Beachten Sie die folgenden Punkte zu bevorzugten Typen:

-   Die DMO gibt möglicherweise einen Typ ohne Formatblock zurück. Beispielsweise könnte ein DMO einen Videotyp angeben, z. B. 24-Bit-RGB, ohne die Breite und Höhe des Bilds anzugeben. Wenn Sie den Typ festlegen, müssen Sie jedoch einen vollständigen Formatblock bereitstellen. (Einige Medientypen, wie z.B. DIE FORMAT-Sperre, erfordern nie einen Formatblock. In diesem Fall gilt dieser Hinweis nicht.)
-   Die DMO ist nicht erforderlich, um jede Kombination von bevorzugten Typen zu unterstützen, die zurückgegeben werden. Wenn ein DMO beispielsweise über zwei Streams verfügt und jeder Stream vier bevorzugte Typen hat, gibt es 16 mögliche Kombinationen, aber nicht alle sind garantiert gültig.
-   Wenn der Client den Medientyp für einen Stream fest legt, DMO die bevorzugten Typen für andere Datenströme entsprechend dem neuen Zustand aktualisiert. Dies ist jedoch nicht erforderlich.
-   Bei einigen Streams bietet die DMO möglicherweise keine bevorzugten Typen. In der Regel sollte DMO-Datenstrom mindestens einige bevorzugte Typen für einige Streams bieten.
-   Die DMO ist nicht erforderlich, um eine vollständige Liste der Medientypen zu bieten, die akzeptiert werden können. Es gibt möglicherweise "nichtvertierte" Typen, die DMO unterstützt, aber nicht als bevorzugte Typen anbieten.

Kurz gesagt, der Client sollte die bevorzugten Typen nur als Richtlinien behandeln. Die einzige Möglichkeit, um zu wissen, welche Typen unterstützt werden, besteht im Testen, wie im nächsten Abschnitt beschrieben.

**Festlegen des Medientyps für einen Stream**

Verwenden Sie [**die Methoden IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) und [**IMediaObject::SetOutputType,**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) um den Typ für jeden Stream fest zu legen. Sie müssen eine **media DMO TYP-Struktur \_ \_** bereitstellen, die eine vollständige Beschreibung des Medientyps enthält. Im folgenden Beispiel wird der Medientyp im Eingabestream 0 mit 44,1 kHz 16-Bit-Stereo-PCM-Audio definiert:


```C++
DMO_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(DMO_MEDIA_TYPE));
// Allocate memory for the format block.
HRESULT hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    // Set the type GUIDs.
    mt.majortype  = MEDIATYPE_Audio;
    mt.subtype    = MEDIASUBTYPE_PCM;
    mt.formattype = FORMAT_WaveFormatEx;

    // Initialize the format block.
    WAVEFORMATEX *pWave = reinterpret_cast<WAVEFORMATEX*>(mt.pbFormat);
    pWave->wFormatTag = WAVE_FORMAT_PCM;
    pWave->nChannels = 2;
    pWave->nSamplesPerSec = 44100;
    pWave->wBitsPerSample = 16;
    pWave->nBlockAlign = (pWave->nChannels * pWave->wBitsPerSample) / 8;
    pWave->nAvgBytesPerSec = pWave->nSamplesPerSec * pWave->nBlockAlign;
    pWave->cbSize = 0;

    // Set the media type.
    hr = pDMO->SetInputType(0, &mt, 0); 

    // Release the format block.
    MoFreeMediaType(&mt);
}
```



Um einen Medientyp zu testen, ohne ihn zu ändern, rufen Sie **SetInputType** oder **SetOutputType** mit dem DMO \_ SET \_ TYPEF \_ TEST \_ ONLY-Flag auf. Die Methode gibt S \_ OK zurück, wenn der Typ akzeptabel ist, andernfalls S \_ FALSE:


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Da sich die Einstellungen für einen Stream auf einen anderen Stream auswirken können, müssen Sie möglicherweise den Medientyp eines Streams löschen. Rufen Sie hierzu **SetInputType** oder **SetOutputType** mit dem DMO \_ SET \_ TYPEF \_ CLEAR-Flag auf.

Für einen Decoder DMO der Client in der Regel zuerst den Eingabetyp festlegen und dann einen Ausgabetyp auswählen. Für einen Encoder DMO der Client zuerst den Ausgabetyp und dann den Eingabetyp festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosten DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



