---
description: Gibt an, wie ein 3D-Videoframe in einem Medienbeispiel gespeichert wird.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat-Attribut (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6529a08c14846fb1d06cd9b3ed0827a43d1b1ba75310c0379efddadebecdaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722870"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MFSampleExtension \_ 3DVideo \_ SampleFormat-Attribut

Gibt an, wie ein 3D-Videoframe in einem Medienbeispiel gespeichert wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein Member der [**MFVideo3DSampleFormat-Enumeration.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat)

Eine Komponente, die 3D-Videoframes generiert, sollte dieses Attribut für jedes Medienbeispiel, das einen 3D-Frame enthält, auf **TRUE** festlegen. Das Attribut wird ignoriert, wenn das [MFSampleExtension \_ 3DVideo-Attribut](mfsampleextension-3dvideo.md) **FALSE** ist oder nicht festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




