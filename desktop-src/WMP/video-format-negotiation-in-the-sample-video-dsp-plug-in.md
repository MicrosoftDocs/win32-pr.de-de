---
title: Aushandlung des Video Formats im Beispiel-Video-DSP-Plug-in
description: Aushandlung des Video Formats im Beispiel-Video-DSP-Plug-in
ms.assetid: 3e92ce10-2b9b-4689-a181-f56c33472fea
keywords:
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, Video formataushandlung
- DSP-Plug-ins, Videoformat Aushandlung
- Video DSP-Plug-ins, Format Aushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287a38fbfcf11f1b9d74087a91c5825b22f1243
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310164"
---
# <a name="video-format-negotiation-in-the-sample-video-dsp-plug-in"></a>Aushandlung des Video Formats im Beispiel-Video-DSP-Plug-in

Bevor Windows Media Player ein Video-DSP-Plug-in in die Signalkette einfügt, muss der Spieler ermitteln, ob das Plug-in das Video verarbeiten kann, das abgespielt wird. Der Prozess, mit dem das Plug-in und der Spieler mit unterstützten Videoformaten kommunizieren, wird als formataushandlung bezeichnet.

## <a name="providing-the-supported-input-and-output-types"></a>Bereitstellen der unterstützten Eingabe-und Ausgabetypen

Wenn das DSP-Plug-in als DirectX Media Object (DMO) fungiert, fragt der Player das Plug-in über die unterstützten Formate ab, indem er eine Sequenz von Aufrufen an **imediaobject:: getinputtype** und **imediaobject:: getoutputtype** sendet.

Wenn das DSP-Plug-in als Media Foundation Transformation (MFT) fungiert, fragt der Spieler das Plug-in über die unterstützten Formate ab, indem es eine Sequenz von Aufrufen von **imftransform:: getinputavailabletype** und **imftransform:: getoutputavailabletype** ausführt.

Das Beispiel-Video-Plug-in, das vom Windows Media Player-Plug-in-Assistenten generiert wird, speichert die Liste der unterstützten Videoformate als Array von GUIDs. Der folgende Code wird aus der Datei "Main. cpp" abgeleitet:


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



Der Player kann **imediaobject:: getinputtype** und **imediaobject:: getoutputtype** in beliebiger Reihenfolge aufrufen, sodass der Plug-in-Code dies vorhersehen muss. Der Spieler kann in beliebiger Reihenfolge **imftransform:: getinputavailabletype** und **imftransform:: getoutputavailabletype** aufrufen. Die Beispiel Implementierungen von **getoutputtype** und **getoutputavailabletype** testen, ob der Eingabetyp bereits definiert wurde. Wenn dies der Fall ist, antwortet das Plug-in, dass es nur diesen Typ unterstützt. Andernfalls gibt das Plug-in den Typ zurück, der dem angegebenen Index entspricht, wie im folgenden Code veranschaulicht:


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



## <a name="setting-the-input-and-output-types"></a>Festlegen der Eingabe-und Ausgabetypen

Wenn das DSP-Plug-in als DMO fungiert, legt Windows Media Player den Medientyp durch Aufrufen von **imediaobject:: setinputtype** und **imediaobject:: setoutputtype** fest und übergibt an jede Funktion einen Zeiger auf eine **DMO- \_ \_ Medientyp** Struktur, die den angeforderten Medientyp darstellt.

Wenn das DSP-Plug-in als MFT fungiert, legt Windows Media Player den Medientyp durch Aufrufen von **imftransform:: setinputtype** und **imftransform:: setoutputtype** fest und übergibt an jede Funktion einen Zeiger auf eine **imfmediatype** -Schnittstelle, die den angeforderten Medientyp darstellt.

Es gibt keine Garantie, dass der Spieler formataushandlungs Methoden in einer bestimmten Reihenfolge aufruft, sodass der Plug-in-Code jeden Fall verarbeiten muss. Wenn der Player beispielsweise **setoutputtype** aufruft, bevor **setinputtype** aufgerufen wird, ist es eine gültige Vorgehensweise, mit der das Plug-in den vorgeschlagenen Ausgabe Medientyp ablehnen kann. Der folgende Code aus der Beispiel Implementierung von **imediaobject:: setoutputtype** veranschaulicht dies:


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



Die Plug-in-Beispiel Implementierungen von **setinputtype** und **setoutputtype** aufrufen die benutzerdefinierte Funktion mit dem Namen **validatemediatype**. Diese Plug-in-Funktion führt eine Reihe von Tests für den vorgeschlagenen Medientyp aus, um sicherzustellen, dass der Medientyp wohl geformt und vom Plug-in unterstützt wird. **Validatemediatype** führt die folgenden Tests aus:

-   Überprüft, ob die Member **majortype** und **Format Type** die korrekten Werte enthalten.
-   Überprüft, ob der **Untertyp** Member mit einem der unterstützten Formate übereinstimmt.
-   Überprüft, ob die Informationen in den Strukturen **BITMAPINFOHEADER** und **videoinfoheader** bzw. **VIDEOINFOHEADER2** gültige Werte enthalten.
-   Testet, ob die Eingabe-und Ausgabemedien Typen Stimmen, da das Plug-in keine Formate von der Eingabe in die Ausgabe konvertiert.

Wenn der vorgeschlagene Medientyp die Validierungstests besteht, wird er in einer Mitgliedsvariablen gespeichert: **m \_ mtinput** für den Eingabe Medientyp, **m \_ mtoutput** für den Ausgabe Medientyp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Video DSP-Plug-ins**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




