---
description: Gibt an, ob die Videointeressierung auf einen Videoframe angewendet wurde.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode-Attribut (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95776fd7b8e130b9538e98843ca72d69980978b6f954747fadca939b8d3c5922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554930"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>MFSampleExtension \_ VideoDSPMode-Attribut

Gibt an, ob die Videointeressierung auf einen Videoframe angewendet wurde.

## <a name="data-type"></a>Datentyp

**MFVideoDSPMode** als **UINT32** gespeichert

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**1000000000**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Hinweise

Der [**Videostabilisierung MFT**](video-stabilization-mft.md) legt dieses Attribut für die ausgabebeispiele fest, die es erzeugt. Der Wert des Attributs ist ein [**MFVideoDSPMode-Enumerationswert.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) Wenn der Wert **MFVideoDSPMode-Stabilisierung \_** ist, bedeutet dies, dass die MFT-Bildstabilisierung auf den Frame angewendet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> <dt>

[**Videostabilisierung MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




