---
description: Festlegen des Medientyps "Gruppe"
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Festlegen des Medientyps "Gruppe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373420"
---
# <a name="setting-the-group-media-type"></a>Festlegen des Medientyps "Gruppe"

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Alle Gruppen müssen einen unkomprimierten Medientyp definieren, entweder Audiodaten oder Videos. Der unkomprimierte Medientyp ist das Format, das Viewer während der Wiedergabe sehen oder hören. In der Regel wird die endgültige Ausgabe in einem komprimierten Format vorliegen. Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).

Um das unkomprimierte Format festzulegen, erstellen Sie eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, und füllen Sie Sie mit dem entsprechenden Haupttyp, Untertyp und Format Header. Weisen Sie für Video eine [**videinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur für den Format Block zu, und legen Sie die Breite, Höhe und Bittiefe fest. Weisen Sie für Audiodaten eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur für den Format Block zu, und legen Sie die Samplingrate, die Bittiefe und die Anzahl der Kanäle fest. Wenn Sie nur den Haupttyp festlegen, stellt der von dem geeignete Standardwerte für die anderen Werte bereit. In der Praxis sollten Sie die Werte explizit festlegen, um die Ausgabe zu steuern.

Nachdem Sie die Medientyp Struktur initialisiert haben, können Sie die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode aufrufen, um den Medientyp für die Gruppe festzulegen.

Im folgenden Beispiel wird ein 16-Bit-RGB-Video mit 320 Pixel breit und 240 Pixel hoch angegeben:


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



Im nächsten Beispiel wird eine Audiogruppe angegeben, indem der Gruppen Medientyp auf einen 16-Bit-Stereo, 44100 Samples pro Sekunde festgelegt wird:


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



Sie können auch die [**cmediatype**](cmediatype.md) -Klasse in den [DirectShow-Basisklassen](directshow-base-classes.md) zum Verwalten von Medientypen verwenden. Sie enthält einige nützliche Hilfsmethoden und gibt den Format Block automatisch frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Medientypen](about-media-types.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 
