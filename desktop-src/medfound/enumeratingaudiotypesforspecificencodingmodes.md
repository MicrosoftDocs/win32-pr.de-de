---
description: Aufzählen von Audiotypen für bestimmte Codierungsmodi
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Aufzählen von Audiotypen für bestimmte Codierungsmodi (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec311c9ac4d879f8834d50353913e7fad1b6e50a9292a44444bc45376247636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828240"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Aufzählen von Audiotypen für bestimmte Codierungsmodi (Microsoft Media Foundation)

Die vom Audioencoder akzeptierten Eingabe- und Ausgabemedientypen sind sehr strukturiert. Sie müssen unterstützte Ausgabetypen abrufen, indem Sie **die IMediaObject::GetOutputType-Methode** oder **DIETRANSFORM::GetOutputType aufrufen.** Nachdem Sie einen Ausgabetyp erhalten haben, dürfen Sie ihn nicht mehr ändern.

Wenn Sie einen anderen Codierungsmodus als 1-Pass-CBR verwenden möchten, müssen Sie den Modus festlegen und dann die Ausgabetypen für diesen Modus aufzählen. Der Encoder ändert die unterstützten Ausgabetypen abhängig vom festgelegten Modus. Die Eigenschaften, die den Codierungsmodus steuern, sind [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) und [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Wenn der Modus im Encoder festgelegt ist, müssen Sie einen Ausgabetyp aufzählen und auswählen und ihn ohne Änderung verwenden, genau wie bei CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identifizieren qualitätsbasierter VBR-Typen

Das Verfahren zum Identifizieren qualitätsbasierter VBR-Typen hängt davon ab, ob der Encoder als DirectX-Medienobjekt (DMO) oder als Media Foundation Transform (MFT) agiert. Informationen dazu, wann ein Encoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte.](codecobjects.md)

Wenn ein Audioencoder als DMO und Sie den Encoder für die Verwendung von VBR mit einem Durchgang konfigurieren, werden alle unterstützten Ausgabetypen aufzählt. Sie sollten jedoch in der Regel einen VBR-Typ mit einem Durchgang basierend auf dem Qualitätsparameter auswählen. Der Encoder legt den Qualitätswert für VBR-Ausgabetypen mit einem Durchgang im **nAvgBytesPerSec-Member** der **WAVEFORMATEX-Struktur** ab, auf die DMO **MEDIA \_ \_ TYPE.pbFormat verweist.**

Dieser Wert wird im folgenden Format gespeichert: 0x7FFFFFXX, wobei XX der Qualitätswert ist (von 0 bis 100). Beispielsweise gibt der **nAvgBytesPerSec-Wert** 0x7FFFFF62 Qualitätsstufe 98 an (0x62 = 98).

Das folgende Beispiel zeigt, wie sie die Qualitätsstufe eines Formats überprüfen, wenn der Encoder als ein DMO.


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



Wenn der Encoder als MFT agiert und bei einem Aufruf von **GetAvailableOutputType** einen Ausgabetyp aufzählt, können Sie MFT nach der **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY-Eigenschaft** abfragen. Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedientyps an. Anschließend können Sie mit diesem Wert die [**MFPKEY \_ DESIRED \_ VBRQUALITY-Eigenschaft**](mfpkey-desired-vbrqualityproperty.md) des Encoders festlegen.

## <a name="setting-peak-constraints"></a>Festlegen von Spitzeneinschränkungen

Für eine qualitätsbasierte VBR (One-Pass) und eine nicht gestützte VBR mit zwei Durchgängen sind nach dem Abrufen des Ausgabetyps keine zusätzlichen Einstellungen erforderlich. Rufen Sie einen Ausgabetyp mit aktivierter VBR und zwei festgelegten Durchläufen ab, um vbr mit Eingeschränkter Spitzenlast zu verwenden. Dieser Typ beschreibt ohne Änderung die nicht trainierten VBR-Einstellungen. Legen Sie zum Festlegen von Spitzeneinschränkungen die [Eigenschaften MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) und [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Audiocodierung](configuringaudioencoding.md)
</dt> <dt>

[Suchen von Audioencoder-Ausgabetypen](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Verwenden Two-Pass Codierung](usingtwoencodingpasses.md)
</dt> <dt>

[Verwenden der VBR-Codierung](usingvbrencoding.md)
</dt> </dl>

 

 



