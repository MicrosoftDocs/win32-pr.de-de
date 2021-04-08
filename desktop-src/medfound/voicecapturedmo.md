---
description: Ein-Objekt, das mehrere DSPs in Bezug auf die sprach Erfassung kapselt.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: Sprach Erfassungs-DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755225"
---
# <a name="voice-capture-dsp"></a>Sprach Erfassungs-DSP

Ein-Objekt, das mehrere DSPs in Bezug auf die sprach Erfassung kapselt.

## <a name="clsid"></a>CLSID

CLSID \_ cwmaudioaec

## <a name="interfaces"></a>Schnittstellen

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>Eigenschaften



| Eigenschaft                                                                                     | BESCHREIBUNG                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [mfpkey \_ wmaaecma- \_ Geräte \_ Indizes](mfpkey-wmaaecma-device-indexesproperty.md)              | Gibt an, welche Audiogeräte der DMO zum Erfassen und Rendern von Audiodaten verwendet.                     |
| [mfpkey \_ wmaaecma \_ devicepair- \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Gibt die Kombination von Audiogeräten an, die zurzeit von der Anwendung verwendet werden.              |
| [mfpkey \_ wmaaecma \_ DMO- \_ Quell \_ Modus](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Gibt an, ob der DMO den Quell Modus oder den Filter Modus verwendet.                                        |
| [mfpkey \_ wmaaecma \_ featr \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Gibt an, wie oft der DMO eine akustische Echo Unterdrückung (AES) für das restliche Signal ausführt. |
| [mfpkey \_ wmaaecma \_ featr \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Gibt an, ob der DMO die automatische Steuerelement Steuerung ausführt.                                        |
| [mfpkey \_ wmaaecma \_ featr \_ Center- \_ Clip](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Gibt an, ob der DMO das zentrale Clipping ausführt.                                               |
| [mfpkey \_ wmaaecma \_ featr- \_ Echo \_ Länge](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Gibt die Dauer von Echo an, die der AEC-Algorithmus (Akustik Echo Abbruch) verarbeiten kann.    |
| [mfpkey \_ wmaaecma \_ featr- \_ Frame \_ Größe](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Gibt die audioframe Größe an.                                                                   |
| [mfpkey \_ wmaaecma \_ featr \_ micarr- \_ Strahl](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Gibt an, welchen Strahl der DMO für die Verarbeitung von mikrofonarrays verwendet.                                |
| [mfpkey \_ wmaaecma \_ featr \_ micarr- \_ Modus](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Gibt an, wie der DMO die Verarbeitung von mikrofonarrays ausführt.                                       |
| [mfpkey \_ wmaaecma \_ featr \_ micarr \_ Preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Gibt an, ob der DMO die Vorverarbeitung eines mikrofonarrays ausführt.                                |
| [mfpkey \_ wmaaecma \_ featr \_ \_ Füll Füll Füll Zeichen](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Gibt an, ob das DMO Füll Füllvorgänge durchführt.                                                 |
| [mfpkey \_ wmaaecma \_ featr \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | Gibt an, ob der DMO eine Rauschunterdrückung durchführt.                                             |
| [mfpkey \_ wmaaecma \_ featr \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Gibt den Typ der sprach Aktivitäts Erkennung an, die vom DMO durchführt wird.                             |
| [mfpkey- \_ wmaaecma- \_ Funktions \_ Modus](mfpkey-wmaaecma-feature-modeproperty.md)                  | Ermöglicht es der Anwendung, die Standardeinstellungen für verschiedene Eigenschaften zu überschreiben.                   |
| [mfpkey \_ wmaaecma \_ MIC-Wert \_ \_ bounter](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Gibt an, ob das DMO die über-und das umgebende Mikrofon anwendet.                                       |
| [mfpkey \_ wmaaecma \_ micarray \_ descptr](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Gibt die Mikrofon Array Geometrie an.                                                          |
| [mfpkey \_ wmaaecma \_ Quality- \_ Metriken](mfpkey-wmaaecma-quality-metricsproperty.md)            | Ruft Qualitätsmetriken für AEC ab.                                                                |
| [mfpkey \_ wmaaecma \_ ruft \_ TS- \_ Statistiken ab](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Gibt an, ob der DMO Zeitstempel Statistiken in der Registrierung speichert.                           |
| [mfpkey- \_ wmaaecma- \_ System \_ Modus](mfpkey-wmaaecma-system-modeproperty.md)                    | Legt den Verarbeitungsmodus fest.                                                                         |



 

## <a name="remarks"></a>Bemerkungen

Im Gegensatz zu anderen DSPs kapselt das sprach Erfassungs Objekt mehrere DSPs in einem einzelnen-Objekt, und das-Objekt ist nur ein DMO-Objekt (es implementiert nicht [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). Die sprach Erfassungs-DMO umfasst die folgenden DSP-Komponenten:

-   Abbruch von akustischem Echo (AEC)
-   Verarbeitung von mikrofonarrays
-   Rauschunterdrückung
-   Automatisches erlangen von Steuerelementen
-   Sprach Aktivitäts Erkennung

Anwendungen können jede Komponente einzeln aktivieren bzw. deaktivieren.

Der sprach Erfassungs-DMO unterstützt zwei Betriebsmodi, den *Filter* Modus und den *Quell* Modus. Im Filter Modus werden von der Anwendung Audiobeispiele vom Mikrofon und von der Sprecher Zeile an den DMO gesendet, und der DMO erzeugt eine Ausgabe.

Im Quell Modus muss die Anwendung keine Beispiele für den DMO bereitstellt. Stattdessen verwaltet der DMO alle Vorgänge auf den Audiogeräten, einschließlich der Initialisierung der Geräte, dem erfassen und Synchronisieren der Audiodatenströme, dem Berechnen von Zeitstempeln und dem Abrufen der Geometrie des mikrofonarrays. Mithilfe des Quell Modus konfiguriert die Anwendung einfach den DMO, und die Ausgabe des DMO ist ein sauberes, verarbeitetes Mikrofonsignal. Der Quell Modus ist wesentlich einfacher zu verwenden als der Filter Modus, und wird für die meisten Anwendungen empfohlen.

Zurzeit unterstützt die sprach Erfassungs-DMO nur einen akustische Echo Abbruch (Single-Channel), sodass die Ausgabe der Redner Zeile einen einzelnen Kanal aufweisen muss. Wenn die Verarbeitung von mikrofonarrays deaktiviert ist, wird die Eingabe mit mehreren Kanälen für die AEC-Verarbeitung auf einen Kanal reduziert. Wenn die Verarbeitung von mikrofonarrays und die AEC-Verarbeitung aktiviert sind, wird AEC vor der Verarbeitung des mikrofonarrays für jedes Mikrofon Element ausgeführt.

### <a name="microphone-array-processing"></a>Verarbeitung von mikrofonarrays

Ein Mikrofon Array ist ein Satz eng positionierter Mikrofone. Mikrofonarrays erzielen eine bessere Direktionalität als ein einzelnes Mikrofon, da die akustischen Wellen bei jedem Mikrofon zu einem etwas anderen Zeitpunkt eintreffen. Weitere Informationen zu mikrofonarrays finden Sie in den Webartikeln [Mikrofon Array Unterstützung in Windows Vista](/windows-hardware/design/component-guidelines/audio) und [Erstellen und Verwenden von mikrofonarrays für Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Verwenden des sprach Erfassungs-DSP

Führen Sie die folgenden Schritte aus, um den sprach Erfassungs-DSP zu verwenden.

### <a name="1-initialize-the-dmo"></a>1. Initialisieren des DMO

Erstellen Sie die sprach Erfassungs-DMO, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit der CLSID- **CLSID \_ cwmaudioaec** aufrufen. Der sprach Erfassungs-dsdp macht nur die Schnittstellen [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) und [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) verfügbar und kann daher nur als DMO verwendet werden.

DMO ist standardmäßig auf den Quell Modus festgelegt. Um den Filter Modus auszuwählen, legen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ DMO \_ Source \_ Mode](mfpkey-wmaaecma-dmo-source-modeproperty.md) auf **Variant \_ false** fest.

Konfigurieren Sie als nächstes die internen Eigenschaften des DMO mithilfe der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle. Die einzige Eigenschaft, die von einer Anwendung festgelegt werden muss, ist die [mfpkey \_ wmaaecma \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md) -Eigenschaft. Diese Eigenschaft konfiguriert die Verarbeitungs Pipeline innerhalb des DMO. Die anderen Eigenschaften sind optional.

### <a name="2-set-the-input-and-output-formats"></a>2. Festlegen der Eingabe-und Ausgabeformate

Wenn Sie DMO im Filter Modus verwenden, legen Sie das Eingabeformat durch Aufrufen von [**imediaobject:: setinputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype)fest. Das Eingabeformat kann fast jeder gültige unkomprimierte PCM oder IEEE-Gleit Komma-Audiotyp sein. Wenn das Eingabeformat nicht mit dem Ausgabeformat identisch ist, führt der DMO automatisch eine Stichproben Raten Konvertierung durch.

Wenn Sie die DMO im Quell Modus verwenden, legen Sie das Eingabeformat nicht fest. Der DMO konfiguriert das Eingabeformat automatisch auf der Grundlage der Audiogeräte.

Legen Sie in beiden Modi das Ausgabeformat durch Aufrufen von [**imediaobject:: setoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)fest. Der DMO kann die folgenden Ausgabeformate akzeptieren:

-   Untertyp: **mediasubtype \_ PCM** oder **mediasubtype \_ IEEE \_ float**
-   Format Block: [**Waveformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) oder [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85))
-   Stichproben pro Sekunde: 8.000; 11.025; 16.000; oder 22.050
-   Kanäle: 1 für den reinen AEC-Modus, 2 oder 4 für die Verarbeitung von mikrofonarrays
-   Bits pro Beispiel: 16

Mit dem folgenden Code wird der Ausgabetyp auf einen 32-Bit-PCM mit einem PCM mit einem einzelnen Kanal


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



### <a name="3-process-data"></a>3. verarbeiten von Daten

Vor der Verarbeitung von Daten empfiehlt es sich, [**imediaobject:: depingestreamingresources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources)aufzurufen. Diese Methode ordnet die Ressourcen zu, die intern vom DMO verwendet werden. Nach den zuvor aufgeführten Schritten, nicht vor, wird "" **zugeordnet** . Wenn Sie diese Methode nicht aufzurufen, ordnet der DMO beim Start der Datenverarbeitung automatisch Ressourcen zu.

Wenn Sie den DMO im Filter Modus verwenden, müssen Sie die Eingabedaten an den DMO übergeben, indem Sie [**imediaobject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)aufrufen. Die Audiodaten des Mikrofons werden an Stream 0 weitergeleitet, und die Audiodaten aus der Redner Linie werden in Stream 1 geleitet. Wenn Sie den DMO im Quell Modus verwenden, müssen Sie **ProcessInput** nicht aufrufen.

Um Ausgabedaten aus dem DSP zu erhalten, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie ein Puffer Objekt, das die Ausgabedaten enthalten soll. Das Buffer-Objekt muss die [**imediabuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) -Schnittstelle implementieren. Die Größe des Puffers hängt von den Anforderungen der Anwendung ab. Wenn Sie einen größeren Puffer zuordnen, können Sie die Wahrscheinlichkeit verringern, dass ein Fehler auftritt.
2.  Deklarieren Sie eine [**DMO- \_ Ausgabe \_ Daten \_ Puffer**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) Struktur, und legen Sie das **pbuffer** -Element auf das Puffer Objekt fest.
3.  Übergeben Sie die [**DMO- \_ Ausgabe \_ Daten \_ Puffer**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) Struktur an die [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) -Methode.
4.  Setzen Sie diese Methode fort, solange der DMO Ausgabedaten enthält. Der DSP signalisiert, dass eine höhere Ausgabe besteht, indem das Flag **DMO \_ Output \_ Data \_ bufferf \_ unvollständiges** Flag im **dwStatus** -Member der [**DMO- \_ Ausgabe \_ Daten \_ Puffer**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) Struktur festgelegt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
