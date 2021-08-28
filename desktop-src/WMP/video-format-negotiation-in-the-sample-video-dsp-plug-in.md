---
title: Videoformataushandlung im Beispielvideo-DSP-Plug-In
description: Videoformataushandlung im Beispielvideo-DSP-Plug-In
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Windows Media Player-Plug-Ins,Video-DSP
- Plug-Ins, Video-DSP
- Plug-Ins für die digitale Signalverarbeitung, Videoformataushandlung
- DSP-Plug-Ins, Videoformataushandlung
- Video-DSP-Plug-Ins, Formataushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90154f3fe7824fb9af563cb662fdcb2847339bc6061d79b3e92cab9c6e36e44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761820"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Videoformataushandlung im Beispielvideo-DSP-Plug-In

Bevor Windows Media Player ein Video-DSP-Plug-In in die Signalkette einfügung, muss der Player bestimmen, ob das Plug-In das abgespielte Video verarbeiten kann. Der Prozess, bei dem das Plug-In und der Player über unterstützte Videoformate kommunizieren, wird als Formataushandlung bezeichnet.

## <a name="providing-the-supported-input-and-output-types"></a>Bereitstellen der unterstützten Eingabe- und Ausgabetypen

Wenn das DSP-Plug-In als DirectX-Medienobjekt (DMO) verwendet wird, fragt der Player das Plug-In nach den unterstützten Formaten ab, indem er eine Folge von Aufrufen von **IMediaObject::GetInputType** und **IMediaObject::GetOutputType vor** sich geht.

Wenn das DSP-Plug-In als Media Foundation-Transformation (MFT) verwendet wird, fragt der Player das Plug-In nach den unterstützten Formaten ab, indem er eine Folge von Aufrufen an **DENTTRANSFORM::GetInputAvailableType** und den 1000111111111111111111118881111555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555555 

Das beispielbasierte Video-Plug-In, das vom Windows Media Player Plug-In-Assistenten generiert wurde, speichert die Liste der unterstützten Videoformate als Array von GUIDs. Der folgende Code wird aus der CPP-Hauptdatei verwendet:


```C++
static const GUID*    k_guidValidSubtypes[] = {
    &MEDIASUBTYPE_NV12,
    &MEDIASUBTYPE_YV12,
    &MEDIASUBTYPE_YUY2,
    &MEDIASUBTYPE_UYVY,
    &MEDIASUBTYPE_RGB32,
    &MEDIASUBTYPE_RGB24,
    &MEDIASUBTYPE RGB555,
    &MEDIASUBTYPE RGB565
};

```



Der Player kann **IMediaObject::GetInputType** und **IMediaObject::GetOutputType** in beliebiger Reihenfolge aufrufen, sodass der Plug-In-Code dies voraussehen muss. Auf ähnliche Weise kann der Player IN beliebiger Reihenfolge **DIEBTRANSFORM::GetInputAvailableType** und **DIETTRANSFORM::GetOutputAvailableType** aufrufen. Die Beispielimplementierungen **von GetOutputType** und **GetOutputAvailableType** testen, ob der Eingabetyp bereits definiert wurde. Wenn dies der Typ ist, antwortet das Plug-In, dass es nur diesen Typ unterstützt. Andernfalls gibt das Plug-In den Typ zurück, der dem angegebenen Index entspricht, wie der folgende Code veranschaulicht:


```C++
// If input type has been defined, then use that as output type.
if (GUID_NULL != m_mtInput.majortype)
{
    hr = ::MoCopyMediaType( pmt, &m_mtInput );
}
else // Otherwise use default for this plug-in.
{
    ::ZeroMemory( pmt, sizeof( DMO_MEDIA_TYPE ) );
    pmt->majortype = MEDIATYPE_Video;
    pmt->subtype = *k_guidValidSubtypes[dwTypeIndex];     
}

```



## <a name="setting-the-input-and-output-types"></a>Festlegen der Eingabe- und Ausgabetypen

Wenn das DSP-Plug-In als DMO verwendet wird, legt Windows Media Player den Medientyp durch Aufrufen von **IMediaObject::SetInputType** und **IMediaObject::SetOutputType** fest. Dabei wird jeder Funktion ein Zeiger auf eine **DMO MEDIA \_ \_ TYPE-Struktur übergeben,** die den angeforderten Medientyp darstellt.

Wenn das DSP-Plug-In als MFT verwendet wird, legt Windows Media Player den Medientyp fest, indem **ERGETransform::SetInputType** und **DANNTransform::SetOutputType** aufruft. Dabei wird jeder Funktion ein Zeiger auf eine **20177-Schnittstelle übergeben,** die den angeforderten Medientyp darstellt.

Es gibt keine Garantie, dass der Player Formataushandlungsmethoden in einer bestimmten Reihenfolge aufruft, daher muss der Plug-In-Code jeden Fall verarbeiten. Wenn der Player beispielsweise **SetOutputType** vor dem Aufruf von **SetInputType** aufruft, ist es eine gültige Aktion für das Plug-In, den vorgeschlagenen Ausgabemedientyp abzulehnen. Der folgende Code aus der Beispielimplementierung von **IMediaObject::SetOutputType** veranschaulicht dies:


```C++
if( GUID_NULL != m_mtInput.majortype )
{
    // Validate that the output media type matches our requirements 
    // and matches our input type (if set).
    hr = ValidateMediaType(pmt, &m_mtInput);
}
else
{
    hr = DMO_E_TYPE_NOT_ACCEPTED;
}

```



Die Beispiel-Plug-In-Implementierungen **von SetInputType** und **SetOutputType** rufen die benutzerdefinierte Funktion mit dem Namen **ValidateMediaType auf.** Diese Plug-In-Funktion führt eine Reihe von Tests für den vorgeschlagenen Medientyp aus, um sicherzustellen, dass der Medientyp wohlgeformt ist und vom Plug-In unterstützt wird. **ValidateMediaType führt** die folgenden Tests aus:

-   Überprüft, ob die **Member majortype und** **formattype** die richtigen Werte enthalten.
-   Überprüft, ob der **Untertyp-Member** einem der unterstützten Formate entspricht.
-   Überprüft, ob die Informationen in den **Strukturen BITMAPINFOHEADER** und **VIDEOINFOHEADER** oder **VIDEOINFOHEADER2** gültige Werte enthalten.
-   Testet, ob die Eingabe- und Ausgabemedientypen übereinstimmen, da das Plug-In keine Formate von der Eingabe in die Ausgabe konvertiert.

Wenn der vorgeschlagene Medientyp die Validierungstests besteht, wird er in einer Membervariablen gespeichert: **m \_ mtInput** für den Eingabemedientyp, **m \_ mtOutput** für den Ausgabemedientyp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video-DSP-Plug-Ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




