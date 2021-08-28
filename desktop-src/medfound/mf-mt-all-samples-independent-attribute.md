---
description: Gibt für einen Medientyp an, ob jedes Beispiel unabhängig von den anderen Stichproben im Stream ist.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT -Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ada34232ccbc7eb30fc9a5bcb64e96542b0375140de426fae951f5e0317c9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060750"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>MF \_ MT ALL SAMPLES \_ \_ \_ INDEPENDENT-Attribut

Gibt für einen Medientyp an, ob jedes Beispiel unabhängig von den anderen Stichproben im Stream ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Wenn dieses Attribut **FALSE ist,** können einige Beispiele nicht ohne Verweis auf andere Beispiele im Stream verwendet werden. Wenn ein Videoformat beispielsweise Deltaframes enthält, sollte dieses Attribut **FALSE sein.**

Dieses Attribut entspricht dem **Feld bTemporalCompression** in der DirectShow [**AM MEDIA \_ \_ TYPE-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Legen Sie dieses Attribut **für alle** nicht komprimierten Medientypen auf TRUE fest.

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEs::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEs::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**VERERBungstyp**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 
