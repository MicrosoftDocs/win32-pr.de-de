---
description: Gibt die bevorzugte Legacy Format Struktur an, die beim Umrechnen eines audiomedientyps verwendet werden soll.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: MF_MT_AUDIO_PREFER_WAVEFORMATEX-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528244"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a>MF \_ \_ -MT-Audiodatei \_ bevorzugt \_ WaveFormatEx-Attribut

Gibt die bevorzugte Legacy Format Struktur an, die beim Umrechnen eines audiomedientyps verwendet werden soll.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut stellt einen Hinweis für die Funktion [**mfkreatewaveformatexfrommfmediatype**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) bereit. Wenn das Attribut **true** ist, konvertiert die-Funktion den audiomedientyp nach Möglichkeit in eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur, anstatt Sie in eine [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur zu konvertieren.

Die Funktion " [**mfinitmediatypeer fromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) " legt dieses Attribut fest. Sie können den Wert dieses Attributs überschreiben. Wenn Sie dieses Attribut auf " **true** " festlegen, wird jedoch nicht sichergestellt, dass ein audiomedientyp in das [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Formular konvertiert werden kann.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 
