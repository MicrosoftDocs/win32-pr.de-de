---
description: Meldet die Metadaten und den Maskenpuffer für eine Hintergrundsegmentierungsmaske, die zwischen Hintergrund und Vordergrund eines Videoframes unterscheidet.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691849"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK-Attribut

Meldet die Metadaten und den Maskenpuffer für eine Hintergrundsegmentierungsmaske, die zwischen Hintergrund und Vordergrund eines Videoframes unterscheidet.

## <a name="data-type"></a>Datentyp

**Blob**

## <a name="remarks"></a>Hinweise

Die von diesem Attribut [](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) übertragenen Daten sind eine KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK-Struktur, die Informationen über die Abmessungen der Hintergrundmaske sowie die Abdeckung des Frames enthält, aus dem sie abgeleitet werden. Dies ist der Frame, der vom Stream ausgegeben wird. Sie enthält auch einen zusammenhängenden Puffer, der die Maske darstellt, die von der nutzenden App genutzt werden soll, um zu definieren, welche Pixel als Teil des Vordergrunds oder Hintergrunds betrachtet werden. Die Skalierungs- und Bildkoordinatenkorrelation der Maske in Bezug auf den Frame wird von der nutzenden App verarbeitet. 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Build 22000t<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Build 22000<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 




