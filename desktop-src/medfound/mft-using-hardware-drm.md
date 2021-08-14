---
description: Gibt an, ob DAS HARDWARE-DRM von DERTRANSFORM-Datei verwendet wird.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473550"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ USING \_ HARDWARE \_ DRM-Attribut

Gibt an, ob DAS HARDWARE-DRM von DERTRANSFORM-Datei verwendet wird.

## <a name="data-type"></a>Datentyp

**UINT32** (als **BOOL** behandelt)

## <a name="getset"></a>Abrufen/Festlegen

Rufen Sie ZUM Abrufen dieses [**Attributs DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Hinweise

Wenn ein MFT-Entschlüsselungsgerät dieses Attribut angibt, das auf 1 festgelegt ist, wird Hardware-DRM verwendet. Wenn ein MFT-Entschlüsselungsgerät dieses Attribut auf 0 festlegt, wird kein Hardware-DRM verwendet. Wenn ein MFT-Entschlüsselungsgerät dieses Attribut nicht oder mit einem anderen Wert angibt, gibt es nicht (oder kann nicht) angeben, ob hardware-DRM verwendet wird.


Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020 Update   <br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Transformieren von Attributen](transform-attributes.md)
</dt> </dl>

 

 




