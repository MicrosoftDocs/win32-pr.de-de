---
description: Festlegen von Medientypen in einem DMO
ms.assetid: 9ff1542d-6a67-414d-8336-aae80c74d5d0
title: Festlegen von Medientypen in einem DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d657977079a75bf5f1eeccc389da6ad67f63b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353631"
---
# <a name="setting-media-types-on-a-dmo"></a>Festlegen von Medientypen in einem DMO

Bevor ein DMO Daten verarbeiten kann, muss der Client den Medientyp für jeden Stream festlegen. (Es gibt eine Ausnahme von dieser Regel, siehe [optionale Streams](optional-streams.md).) Um die Anzahl der Streams zu ermitteln, müssen Sie die [**imediaobject:: getstreamcount**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getstreamcount) -Methode aufrufen:


```C++
DWORD cInput = 0, cOutput = 0;
pDMO->GetStreamCount(&cInput, &cOutput);
```



Diese Methode gibt zwei Werte zurück, die Anzahl der Eingaben und die Anzahl der Ausgaben. Diese Werte sind für die Lebensdauer des DMO fest.

**Bevorzugte Typen**

Der DMO weist für jeden Stream eine Liste möglicher Medientypen in der angegebenen Reihenfolge zu. Die bevorzugten Typen können z. b. 32-RGB, 24-Bit-RGB und 16-Bit-RGB in dieser Reihenfolge sein. Wenn die Medientypen vom Client festgelegt werden, können diese Listen als Hinweis verwendet werden. Um einen bevorzugten Typ für einen Stream abzurufen, rufen Sie die [**imediaobject:: getinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) -Methode oder die [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) -Methode auf. Geben Sie die Datenstrom Nummer und einen Indexwert für den Typ an (beginnend bei null). Der folgende Code ruft beispielsweise den ersten bevorzugten Typ aus dem ersten Eingabedaten Strom ab:


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



Um alle bevorzugten Medientypen für einen bestimmten Stream aufzulisten, verwenden Sie eine-Schleife, die den Typindex Inkremente erhöht, bis die-Methode DMO \_ E \_ ohne \_ Weitere Elemente zurückgibt \_ , wie im folgenden Beispiel gezeigt:


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

-   Der DMO gibt möglicherweise einen Typ zurück, der über keinen Format Block verfügt. Ein DMO könnte z. b. einen Videotyp, z. b. 24-Bit-RGB, angeben, ohne die Breite und Höhe des Bilds bereitzustellen. Wenn Sie den Typ festlegen, müssen Sie jedoch einen kompletten Format Block bereitstellen. (Einige Medientypen, z. b. "MIDI", benötigen nie einen Format Block. in diesem Fall gilt diese Anmerkung nicht.)
-   Der DMO muss nicht jede Kombination von bevorzugten Typen unterstützen, die er zurückgibt. Wenn ein DMO z. b. über zwei Streams verfügt und jeder Stream vier bevorzugte Typen aufweist, gibt es 16 mögliche Kombinationen, aber nicht alle davon sind gültig.
-   Wenn der Client den Medientyp für einen Stream festlegt, kann der DMO die bevorzugten Typen für andere Streams aktualisieren, um den neuen Zustand widerzuspiegeln. Dies ist jedoch nicht erforderlich.
-   Für einige Streams bietet der DMO möglicherweise keine bevorzugten Typen. In der Regel sollte ein DMO in einigen Streams zumindest einige bevorzugte Typen anbieten.
-   Der DMO ist nicht erforderlich, um eine komplette Liste der Medientypen, die akzeptiert werden können, bereitzustellen. Möglicherweise gibt es "nicht angekündigte" Typen, die der DMO unterstützt, aber nicht als bevorzugte Typen anbietet.

Kurz gesagt, der Client sollte die bevorzugten Typen nur als Richtlinien behandeln. Die einzige Möglichkeit, herauszufinden, welche Typen unterstützt werden, besteht darin, Sie zu testen, wie im nächsten Abschnitt beschrieben.

**Festlegen des Medientyps in einem Stream**

Verwenden Sie die Methoden [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) und [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) , um den Typ für jeden Stream festzulegen. Sie müssen eine **DMO- \_ \_ Medientyp** Struktur bereitstellen, die eine umfassende Beschreibung des Medientyps enthält. Im folgenden Beispiel 44,1 wird der Medientyp für den Eingabedaten Strom 0 festgelegt


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



Um einen Medientyp zu testen, ohne ihn festzulegen, müssen Sie **setinputtype** oder **setoutputtype** mit dem Flag DMO \_ Set \_ typef \_ Test \_ only aufrufen. Die Methode gibt "s OK" zurück \_ , wenn der Typ akzeptabel ist, \_ andernfalls "false":


```C++
if (S_OK == pDMO->SetInputType(0, &mt, DMO_SET_TYPEF_TEST_ONLY)
{
    // Media type is OK.
}
```



Da sich die Einstellungen in einem Datenstrom auf einen anderen Stream auswirken können, müssen Sie möglicherweise den Medientyp eines Streams löschen. Aufrufen Sie hierzu **setinputtype** oder **setoutputtype** mit dem Flag DMO \_ Set \_ typef \_ Clear.

Bei einem decoderdmo würde der Client in der Regel zuerst den Eingabetyp festlegen und dann einen Ausgabetyp auswählen. Bei einem Encoder-DMO würde der Client zuerst den Ausgabetyp und dann den Eingabetyp festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direktes Hosting eines DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



