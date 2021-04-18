---
description: Gibt für einen Medientyp an, ob jede Stichprobe unabhängig von den anderen Beispielen im Stream ist.
ms.assetid: 40434f63-e191-45e1-b788-5f80fe7f49ae
title: MF_MT_ALL_SAMPLES_INDEPENDENT-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82173e99a30e033b3d90f6cfec0dc2aa8b3af97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354599"
---
# <a name="mf_mt_all_samples_independent-attribute"></a>MF \_ MT \_ All \_ Samples \_ Independent Attribute

Gibt für einen Medientyp an, ob jede Stichprobe unabhängig von den anderen Beispielen im Stream ist.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Wenn dieses Attribut **false** ist, können einige Beispiele nicht verwendet werden, ohne auf andere Beispiele im Stream zu verweisen. Wenn ein Videoformat z. b. Delta Rahmen enthält, sollte dieses Attribut " **false**" lauten.

Dieses Attribut entspricht dem Feld **btemporalcompression** in der Struktur des DirectShow [**am- \_ Medien \_ Typs**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Legen Sie dieses Attribut für alle nicht komprimierten Medientypen auf **true** fest.

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

 

 
