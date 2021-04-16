---
description: Gibt an, ob IMF Transform Hardware DRM verwendet.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485347"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ mithilfe des \_ Hardware-DRM- \_ Attributs

Gibt an, ob IMF Transform Hardware DRM verwendet.

## <a name="data-type"></a>Datentyp

**UInt32** (als **bool** behandelt)

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imtransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Bemerkungen

Wenn eine MFT-Entschlüsselung angibt, dass dieses Attribut auf 1 festgelegt ist, wird Hardware-DRM verwendet. Wenn eine MFT-Entschlüsselung angibt, dass dieses Attribut auf 0 festgelegt ist, wird das Hardware-DRM nicht verwendet. Wenn eine MFT-Entschlüsselung dieses Attribut nicht angibt oder es mit einem anderen Wert angibt, kann Sie nicht angeben, ob Sie Hardware-DRM verwendet.


Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 April 2020-Update   <br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Transformations Attribute](transform-attributes.md)
</dt> </dl>

 

 




