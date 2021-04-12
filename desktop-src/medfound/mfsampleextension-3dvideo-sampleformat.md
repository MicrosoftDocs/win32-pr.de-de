---
description: Gibt an, wie ein 3D-Videoframe in einem Medien Beispiel gespeichert wird.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131128"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>MF Sample Extension \_ 3dvideo \_ Sampleformat-Attribut

Gibt an, wie ein 3D-Videoframe in einem Medien Beispiel gespeichert wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein Member der [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) -Enumeration.

Eine Komponente, die 3D-Video Frames generiert, sollte dieses Attribut für jedes Medien Beispiel, das einen 3D-Frame enthält, auf " **true** " festlegen. Das Attribut wird ignoriert, wenn das Attribut " [MF Sample Extension \_ 3dvideo](mfsampleextension-3dvideo.md) " den Wert " **false** " hat oder nicht festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MF Sample Extension \_ 3dvideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




