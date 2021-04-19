---
description: Anzahl von Audiobeispielen, die in einem komprimierten Block von Audiodaten enthalten sind. Dieses Attribut kann in komprimierten Audioformaten verwendet werden, die über eine festgelegte Anzahl von Stichproben in jedem Block verfügen.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: MF_MT_AUDIO_SAMPLES_PER_BLOCK-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363233"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a>MF \_ \_ -MT- \_ Audiobeispiele \_ pro Block- \_ Attribut

Anzahl von Audiobeispielen, die in einem komprimierten Block von Audiodaten enthalten sind. Dieses Attribut kann in komprimierten Audioformaten verwendet werden, die über eine festgelegte Anzahl von Stichproben in jedem Block verfügen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut entspricht dem **wsamplesperblock** -Member der [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur.

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

 

 
