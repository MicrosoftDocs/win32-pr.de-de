---
description: Gibt an, ob ein Puffer den Anfang eines ASF-Pakets (Advanced Systems Format) enthält.
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY-Attribut (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0904c6b5a002d6aa18361365946a176521674ea22f7a45cc042b89d844c4210d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464060"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>MFASFSPLITTER \_ PACKET \_ BOUNDARY-Attribut

Gibt an, ob ein Puffer den Anfang eines ASF-Pakets (Advanced Systems Format) enthält.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Wenn ein Medienpuffer die [**INTERFACESAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) über **QueryInterface** verfügbar macht und der Wert dieses Attributs ungleich 0 (null) ist, behandelt der ASF-Splitter den Puffer als Anfang eines neuen Pakets.

Dieses Attribut gilt, wenn Sie den ASF-Splitter zum Analysieren von ASF-Daten verwenden. Wenn Ihre ASF-Daten variable Paketlängen aufweisen, müssen Sie dieses Attribut für die Medienpuffer festlegen, die Sie an die [**IMFASFSplitter::P arseData-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) übergeben. Legen Sie das Attribut auf **TRUE** fest, wenn der Puffer den Anfang eines neuen Pakets enthält. Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das -Attribut auf **FALSE** fest. Die Puffer können sich nicht über mehrere Pakete erstrecken.

Für ASF-Daten mit festen Paketgrößen ist dieses Attribut nicht erforderlich, und ein Puffer kann mehrere Pakete umfassen.

Beachten Sie, dass die von Media Foundation bereitgestellten Standardimplementierungen des [**VOM**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Media Foundation [**NICHT DIE ATTRIBUTEAttribute verfügbar**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)machen. Um dieses Attribut verwenden zu können, müssen Sie Ihre eigene Implementierung von **ÜBERMEDIABUFFER** bereitstellen. z. B. durch Umschließen der Puffer, die von [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer)zurückgegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[ASF-Attribute](asf-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**BUFFERMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




