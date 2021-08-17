---
description: Gibt den Kernelstreamingbezeichner (KS) für einen Stream auf einem Videoaufnahmegerät an.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: MF_DEVICESTREAM_STREAM_ID-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb5b4004ae2e280806411e51f7adfe83f9a4f28d71103a3d3c6e9a247f2011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973849"
---
# <a name="mf_devicestream_stream_id-attribute"></a>MF \_ \_ DEVICESTREAM-STREAM-ID-Attribut \_

Gibt den Kernelstreamingbezeichner (KS) für einen Stream auf einem Videoaufnahmegerät an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Gehen Sie wie folgt vor, um dieses Attribut abzurufen:

1.  Fragen Sie die Medienquelle nach der [**SCHNITTSTELLE "CSVMediaSourceEx"**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) ab.
2.  Rufen Sie [**DEN CURSORMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**POINTERAttributes-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für den Stream abzurufen.
3.  Rufen Sie [**DIE ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) auf, um das Attribut abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




