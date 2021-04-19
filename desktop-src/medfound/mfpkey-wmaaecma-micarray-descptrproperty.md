---
description: Gibt die Mikrofon Array Geometrie für den sprach Erfassungs-DSP an.
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: MFPKEY_WMAAECMA_MICARRAY_DESCPTR-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355571"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a>Mfpkey \_ wmaaecma \_ micarray \_ descptr (Eigenschaft)

Gibt die Mikrofon Array Geometrie für den sprach Erfassungs-DSP an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT- \_ BLOB

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist eine [**kston- \_ MIC- \_ array \_ Geometrie**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) Struktur. Diese Struktur wird in der Header Datei "ksmedia. h" definiert. Um die Geometrie des mikrofonarrays abzurufen, Fragen Sie das Audiogerät nach der Geometry-Eigenschaft des ksproperty \_ - \_ audiomic-Arrays ab, \_ indem Sie \_ die Methode " **ikscontrol:: ksproperty** " auf dem Gerät aufrufen. Weitere Informationen zu mikrofonarrays finden Sie im Whitepaper [Erstellen und Verwenden von mikrofonarrays für Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filter Modus verwenden und die Verarbeitung von mikrofonarrays aktiviert ist. Wenn Sie den DSP im Quell Modus verwenden, fragt der DSP das Gerät automatisch nach den Geometry-Informationen ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
