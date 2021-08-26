---
description: Festlegen des Gruppenmedientyps
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Festlegen des Gruppenmedientyps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c758e089a4f1240debb14c8159d039380b3473991860fef54470c12c1c00b1e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928180"
---
# <a name="setting-the-group-media-type"></a>Festlegen des Gruppenmedientyps

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Alle Gruppen müssen einen nicht komprimierten Medientyp definieren, entweder Audio oder Video. Der nicht komprimierte Medientyp ist das Format, das der Betrachter während der Wiedergabe sehen oder hören kann. In der Regel wird die endgültige Ausgabe in einem komprimierten Format ausgegeben. Weitere Informationen finden Sie unter [Rendern eines Project](rendering-a-project.md).

Um das nicht komprimierte Format festzulegen, erstellen Sie eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) und füllen Sie sie mit dem entsprechenden Haupttyp, Untertyp und Formatheader aus. Ordnen Sie für Video eine [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) für den Formatblock zu, und legen Sie Breite, Höhe und Bittiefe fest. Ordnen Sie für Audio eine [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) für den Formatblock zu, und legen Sie die Abtastrate, Bittiefe und Anzahl von Kanälen fest. Wenn Sie nur den Haupttyp festlegen, stellt DES sinnvolle Standardwerte für die anderen Werte bereit. In der Praxis sollten Sie die Werte explizit festlegen, um die Ausgabe zu steuern.

Nachdem Sie die Medientypstruktur initialisiert haben, rufen Sie die [**IAMTimelineGroup::SetMediaType-Methode**](iamtimelinegroup-setmediatype.md) auf, um den Medientyp für die Gruppe festzulegen.

Im folgenden Beispiel wird ein 16-Bit-RGB-Video mit einer Breite von 320 x 240 Pixeln angegeben:


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



Im nächsten Beispiel wird eine Audiogruppe angegeben, indem der Medientyp der Gruppe auf 16-Bit-Stereo und 44.100 Stichproben pro Sekunde festgelegt wird:


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



Sie können auch die [**CMediaType-Klasse**](cmediatype.md) in den [DirectShow-Basisklassen](directshow-base-classes.md) verwenden, um Medientypen zu verwalten. Sie enthält einige nützliche Hilfsmethoden und gibt den Formatblock automatisch frei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Medientypen](about-media-types.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 
