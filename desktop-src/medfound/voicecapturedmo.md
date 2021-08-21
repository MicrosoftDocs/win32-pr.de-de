---
description: Ein Objekt, das mehrere DSPs im Zusammenhang mit der Spracherfassung kapselt.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: Spracherfassungs-DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d05eb6d3f97f748d5c82d8fa566ee25a3a01ce225ab76e84d73f0a86b132afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972549"
---
# <a name="voice-capture-dsp"></a>Spracherfassungs-DSP

Ein Objekt, das mehrere DSPs im Zusammenhang mit der Spracherfassung kapselt.

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>Schnittstellen

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **Ipropertystore**

## <a name="properties"></a>Eigenschaften



| Eigenschaft                                                                                     | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [MFPKEY \_ \_ WMAAECMA-GERÄTEINDIZES \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Gibt an, welche Audiogeräte vom DMO zum Erfassen und Rendern von Audio verwendet werden.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifiziert die Kombination von Audiogeräten, die die Anwendung derzeit verwendet.              |
| [MFPKEY \_ WMAAECMA \_ DMO \_ \_ QUELLMODUS](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Gibt an, ob der DMO den Quell- oder Filtermodus verwendet.                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Gibt an, wie oft das DMO AES (Acoustic Echo Suppression) für das Restsignal ausführt. |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Gibt an, ob die DMO automatische Verstärkungssteuerung ausführt.                                        |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ CENTER \_ CLIP](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Gibt an, ob der DMO zentriert abgeschnitten wird.                                               |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Gibt die Dauer des Echos an, die der AEC-Algorithmus (Acoustic Echo Cancellation) verarbeiten kann.    |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Gibt die Audioframegröße an.                                                                   |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR-BALKEN \_](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Gibt an, welcher Balken der DMO für die Mikrofonarrayverarbeitung verwendet.                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Gibt an, wie der DMO die Mikrofonarrayverarbeitung ausführt.                                       |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Gibt an, ob die DMO die Vorverarbeitung des Mikrofonarrays ausführt.                                |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NOISE \_ FILL](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Gibt an, ob die DMO eine Füllfüllung ausführt.                                                 |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | Gibt an, ob die DMO Rauschunterdrückung ausführt.                                             |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Gibt den Typ der Sprachaktivitätserkennung an, die vom DMO ausgeführt wird.                             |
| [MFPKEY \_ \_ WMAAECMA-FEATUREMODUS \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Ermöglicht der Anwendung, die Standardeinstellungen für verschiedene Eigenschaften zu überschreiben.                   |
| [MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Gibt an, ob die DMO die Mikrofongewinngrenze anwendet.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Gibt die Geometrie des Mikrofonarrays an.                                                          |
| [MFPKEY \_ WMAAECMA \_ QUALITY \_ METRICS](mfpkey-wmaaecma-quality-metricsproperty.md)            | Ruft Qualitätsmetriken für AEC ab.                                                                |
| [MFPKEY \_ WMAAECMA \_ – ABRUFEN VON \_ \_ TS-STATISTIKEN](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Gibt an, ob die DMO Zeitstempelstatistiken in der Registrierung speichert.                           |
| [MFPKEY \_ \_ WMAAECMA-SYSTEMMODUS \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Legt den Verarbeitungsmodus fest.                                                                         |



 

## <a name="remarks"></a>Hinweise

Im Gegensatz zu den anderen DSPs kapselt das Spracherfassungsobjekt mehrere DSPs in einem einzelnen -Objekt, und das -Objekt ist nur ein DMO -Objekt (es implementiert NICHT [**DIESTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). Die Spracherfassung DMO umfasst die folgenden DSP-Komponenten:

-   Akustik-Echoabbruch (Acoustic Echo Cancellation, AEC)
-   Mikrofonarrayverarbeitung
-   Rauschunterdrückung
-   Steuerung der automatischen Verstärkung
-   Erkennung von Sprachaktivitäten

Anwendungen können jede Komponente einzeln aktivieren und deaktivieren.

Die Spracherfassung DMO unterstützt zwei Betriebsmodi: *den Filtermodus* und den *Quellmodus.* Im Filtermodus sendet die Anwendung Audiobeispiele vom Mikrofon und von der Lautsprecherzeile an die DMO, und die DMO erzeugt eine Ausgabe.

Im Quellmodus muss die Anwendung keine Beispiele an die DMO übermitteln. Stattdessen verwaltet der DMO alle Vorgänge auf den Audiogeräten, einschließlich initialisieren der Geräte, Erfassen und Synchronisieren der Audiostreams, Berechnen von Zeitstempeln und Abrufen der Geometrie des Mikrofonarrays. Im Quellmodus konfiguriert die Anwendung einfach die DMO, und die Ausgabe des DMO ist ein sauberes, verarbeitetes Mikrofonsignal. Der Quellmodus ist deutlich einfacher zu verwenden als der Filtermodus und wird für die meisten Anwendungen empfohlen.

Derzeit unterstützt die Spracherfassung DMO nur AEC (Acoustic Echo Cancellation, AEC) mit einem Kanal, sodass die Ausgabe der Lautsprecherzeile einkanalig sein muss. Wenn die Mikrofonarrayverarbeitung deaktiviert ist, wird die Multikanaleingabe für die AEC-Verarbeitung auf einen Kanal heruntergeklappt. Wenn sowohl die Mikrofonarrayverarbeitung als auch die AEC-Verarbeitung aktiviert sind, wird AEC für jedes Mikrofonelement vor der Mikrofonarrayverarbeitung ausgeführt.

### <a name="microphone-array-processing"></a>Mikrofonarrayverarbeitung

Ein Mikrofonarray ist ein Satz eng positionierter Mikrofone. Mikrofonarrays erzielen eine bessere Richtung als ein einzelnes Mikrofon, da die Akustikwellen zu einem etwas anderen Zeitpunkt an jedem Mikrofon eintreffen. Weitere Informationen zu Mikrofonarrays finden Sie in den Webartikeln [Mikrofonarrayunterstützung in Windows Vista](/windows-hardware/design/component-guidelines/audio) und [Erstellen und Verwenden von Mikrofonarrays für Windows Vista.](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)

### <a name="using-the-voice-capture-dsp"></a>Verwenden des Spracherfassungs-DSP

Führen Sie die folgenden Schritte aus, um den Spracherfassungs-DSP zu verwenden.

### <a name="1-initialize-the-dmo"></a>1. Initialisieren des DMO

Erstellen Sie die Spracherfassung DMO, indem [**Sie CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit der **CLSID CLSID \_ CWMAudioAEC** aufrufen. Der Spracherfassungs-DSDP macht nur die [**IMediaObject-**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) und [**IPropertyStore-Schnittstellen**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar, sodass er nur als DMO verwendet werden kann.

Der DMO wird standardmäßig in den Quellmodus versetzt. Um den Filtermodus auszuwählen, legen Sie [MFPKEY \_ WMAAECMA \_ DMO SOURCE \_ \_ MODE-Eigenschaft](mfpkey-wmaaecma-dmo-source-modeproperty.md) auf **VARIANT FALSE \_ fest.**

Konfigurieren Sie als Nächstes die internen Eigenschaften des DMO mithilfe der [**IPropertyStore-Schnittstelle.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Die einzige Eigenschaft, die eine Anwendung festlegen muss, ist die [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE-Eigenschaft.](mfpkey-wmaaecma-system-modeproperty.md) Diese Eigenschaft konfiguriert die Verarbeitungspipeline innerhalb des DMO. Die anderen Eigenschaften sind optional.

### <a name="2-set-the-input-and-output-formats"></a>2. Festlegen der Eingabe- und Ausgabeformate

Wenn Sie die DMO im Filtermodus verwenden, legen Sie das Eingabeformat fest, indem [**Sie IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype)aufrufen. Das Eingabeformat kann fast jeder gültige unkomprimierte PCM- oder IEEE-Gleitkommaaudiotyp sein. Wenn das Eingabeformat nicht mit dem Ausgabeformat übereinstimmt, führt der DMO automatisch eine Beispielratenkonvertierung durch.

Wenn Sie die DMO im Quellmodus verwenden, legen Sie das Eingabeformat nicht fest. Der DMO konfiguriert automatisch das Eingabeformat basierend auf den Audiogeräten.

Legen Sie in beiden Modi das Ausgabeformat fest, indem [**Sie IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)aufrufen. Die DMO können die folgenden Ausgabeformate akzeptieren:

-   Untertyp: **MEDIASUBTYPE \_ PCM** oder **MEDIASUBTYPE \_ IEEE \_ FLOAT**
-   Formatblock: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) oder [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Stichproben pro Sekunde: 8.000; 11,025; 16,000; oder 22.050
-   Kanäle: 1 für den reinen AEC-Modus, 2 oder 4 für die Verarbeitung von Mikrofonarrays
-   Bits pro Beispiel: 16

Der folgende Code legt den Ausgabetyp auf 16-Bit-PCM-Audio mit einem Kanal fest:


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. Verarbeiten von Daten

Vor der Verarbeitung von Daten wird empfohlen, [**IMediaObject::AllocateStreamingResources auf aufruft.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) Diese Methode ordnet die ressourcen zu, die intern vom -DMO. Rufen **Sie AllocateStreamingResources nach den** zuvor aufgeführten Schritten auf, nicht zuvor. Wenn Sie diese Methode nicht aufrufen, weist DMO automatisch Ressourcen zu, wenn die Datenverarbeitung beginnt.

Wenn Sie die DMO im Filtermodus verwenden, müssen Sie Eingabedaten an die DMO übergeben, indem Sie [**IMediaObject::P rocessInput aufrufen.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) Die Audiodaten vom Mikrofon werden in Stream 0 übertragen, und die Audiodaten aus der Lautsprecherzeile werden in Stream 1 übertragen. Wenn Sie die -DMO im Quellmodus verwenden, müssen Sie **ProcessInput nicht aufrufen.**

Führen Sie die folgenden Schritte aus, um Ausgabedaten aus dem DSP zu erhalten:

1.  Erstellen Sie ein Pufferobjekt, das die Ausgabedaten enthält. Das Pufferobjekt muss die [**IMediaBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) implementieren. Die Größe des Puffers hängt von den Anforderungen Ihrer Anwendung ab. Das Zuweisen eines größeren Puffers kann die Wahrscheinlichkeit von Störungen verringern.
2.  Deklarieren [**Sie DMO OUTPUT DATA \_ \_ \_ BUFFER-Struktur,**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) und legen Sie den **pBuffer-Member** so fest, dass er auf Ihr Pufferobjekt zeigen soll.
3.  Übergeben Sie [**DMO \_ OUTPUT DATA \_ \_ BUFFER-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) an die [**IMediaObject::P rocessOutput-Methode.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)
4.  Fahren Sie mit dem Aufrufen dieser Methode fort, solange die DMO Ausgabedaten hat. Der DSP signalisiert, dass er über mehr Ausgabe verfügt, indem er das flag **DMO \_ OUTPUT DATA \_ \_ BUFFERF \_ INCOMPLETE** im **dwStatus-Member** der DMO [**OUTPUT DATA \_ \_ \_ BUFFER-Struktur**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signalprozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
