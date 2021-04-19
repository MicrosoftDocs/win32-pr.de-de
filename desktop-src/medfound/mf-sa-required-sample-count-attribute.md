---
description: Gibt die Anzahl von nicht komprimierten Puffern an, die von der gesteigerten Video-Renderer (EVR) für Deinterlacing benötigt werden.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: MF_SA_REQUIRED_SAMPLE_COUNT-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351753"
---
# <a name="mf_sa_required_sample_count-attribute"></a>\_ \_ Anzahl erforderlicher \_ \_ Attribute der MF-SA

Gibt die Anzahl von nicht komprimierten Puffern an, die von der gesteigerten Video-Renderer (EVR) für Deinterlacing benötigt werden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um ein Attribut auf Streamebene. Gehen Sie folgendermaßen vor, um das-Attribut aus dem EVR zu erhalten:

1.  Aufrufen von [**imfmediasink:: getstreamsinkbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) zum Abrufen der streamsenke.
2.  Abfragen der streamsenke für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.
3.  Rückrufe [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Intern wird dieses Attribut vom Mixer dem EVR bereitstellt. Um das Attribut vom Mixer abzurufen, nennen Sie [**imftransform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 




