---
description: Auflisten von Audiotypen für bestimmte Codierungs Modi
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Auflisten von Audiotypen für bestimmte Codierungs Modi (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393269"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a>Auflisten von Audiotypen für bestimmte Codierungs Modi (Microsoft Media Foundation)

Die vom Audioencoder akzeptierten Eingabe-und Ausgabemedien Typen sind sehr strukturiert. Sie müssen unterstützte Ausgabetypen abrufen, indem Sie die **imediaobject:: getoutputtype** -Methode oder **imftransform:: getoutputtype** aufrufen. Nachdem Sie einen Ausgabetyp erhalten haben, dürfen Sie ihn nicht mehr ändern.

Wenn Sie einen anderen Codierungs Modus als einen einzigen Pass-CBR verwenden möchten, müssen Sie den-Modus festlegen und dann die Ausgabetypen für diesen Modus auflisten. der Encoder ändert die unterstützten Ausgabetypen, je nachdem, welcher Modus festgelegt wurde. Die Eigenschaften, die den Codierungs Modus steuern, sind [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) und [**mfpkey \_ passesused**](mfpkey-passesusedproperty.md). Wenn der Modus im Encoder festgelegt ist, müssen Sie einen Ausgabetyp ohne Änderung auflisten und auswählen, ebenso wie bei CBR.

## <a name="identifying-quality-based-vbr-types"></a>Identifizieren von Qualitäts basierten VBR-Typen

Die Vorgehensweise zum Identifizieren von Qualitäts basierten VBR-Typen hängt davon ab, ob der Encoder als DirectX Media Object (DMO) fungiert oder als Media Foundation Transform (MFT) fungiert. Informationen dazu, wann ein Encoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).

Wenn ein Audioencoder als DMO fungiert und Sie den Encoder für die Verwendung von One-Pass-VBR konfigurieren, listet er alle unterstützten Ausgabetypen auf. Allerdings möchten Sie in der Regel einen 1-Pass-VBR-Typ auf Grundlage des Quality-Parameters auswählen. Der Encoder legt den Qualitäts Wert für einstufige VBR-Ausgabetypen im **navgbytespersec** -Member der **WaveFormatEx** -Struktur ab, auf die durch **DMO \_ Media \_ Type. pbformat** verwiesen wird.

Dieser Wert wird in folgendem Format gespeichert: 0x7fffffxx, wobei XX der Qualitäts Wert ist (von 0 bis 100). Beispielsweise wird mit dem **navgbytespersec** -Wert 0x7fffff62 der Qualitätsgrad 98 (0x62 = 98) angegeben.

Im folgenden Beispiel wird gezeigt, wie die Qualitätsstufe eines Formats überprüft wird, wenn der Encoder als DMO fungiert.


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



Wenn der Encoder als MFT fungiert und einen Ausgabetyp bei einem Aufrufen von **getavailableoutputtype** auflistet, können Sie die MFT für die zuletzt **\_ \_ \_ aufgelistete \_ vbrquality-Eigenschaft von mfpkey** Abfragen. Der zurückgegebene Wert gibt die VBR-Qualität des zuletzt zurückgegebenen Ausgabemedien Typs an. Anschließend können Sie diesen Wert verwenden, um die [**\_ gewünschte \_ Eigenschaft "mfpkey**](mfpkey-desired-vbrqualityproperty.md) " des Encoders festzulegen.

## <a name="setting-peak-constraints"></a>Festlegen von Spitzen Einschränkungen

Bei Qualitäts basierter VBR (One-Pass) und uneingeschränkter 2-Pass-VBR sind nach dem Abrufen des Ausgabe Typs keine weiteren Einstellungen erforderlich. Wenn Sie VBR mit hoher Last verwenden möchten, rufen Sie einen Ausgabetyp mit aktiviertem VBR und zwei Durchläufen ab. Dieser Typ beschreibt ohne Änderung die nicht eingeschränkten VBR-Einstellungen. Legen Sie zum Festlegen von Spitzen Einschränkungen die Eigenschaften [mfpkey \_ Rmax](mfpkey-rmaxproperty.md) und [mfpkey \_ bmax](mfpkey-bmaxproperty.md) fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren der Audiocodierung](configuringaudioencoding.md)
</dt> <dt>

[Suchen von Audioencoder-Ausgabetypen](findingaudioencoderoutputtypes.md)
</dt> <dt>

[Verwenden von Two-Pass Codierung](usingtwoencodingpasses.md)
</dt> <dt>

[Verwenden der VBR-Codierung](usingvbrencoding.md)
</dt> </dl>

 

 



