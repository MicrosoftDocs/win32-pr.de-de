---
description: Gibt die Geometrie des Mikrofonarrays für den Spracherfassungs-DSP an.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2bf0b495e7b57ba60cf5cc993b85a143836c8666e06d6b849ece3693b2a334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722944"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR-Eigenschaft

Gibt die Geometrie des Mikrofonarrays für den Spracherfassungs-DSP an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

\_VT-BLOB

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist eine [**KSAUDIO \_ MIC \_ ARRAY \_ GEOMETRY-Struktur.**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) Diese Struktur wird in der Headerdatei KsMedia.h definiert. Um die Geometrie des Mikrofonarrays abzurufen, fragen Sie das Audiogerät nach der KSPROPERTY \_ AUDIO \_ MIC ARRAY \_ \_ GEOMETRY-Eigenschaft ab, indem Sie die **IKsControl::KSProperty-Methode** auf dem Gerät aufrufen. Weitere Informationen zu Mikrofonarrays können Sie im Whitepaper [How to Build and Use Microphone Arrays for Windows Vista (Erstellen und Verwenden von Mikrofonarrays für Windows Vista)](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)herunterladen.

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filtermodus verwenden und die Verarbeitung des Mikrofonarrays aktiviert ist. Wenn Sie den DSP im Quellmodus verwenden, fragt der DSP automatisch die Geometrieinformationen für das Gerät ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
