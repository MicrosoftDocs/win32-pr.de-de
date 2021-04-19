---
description: Gibt an, ob einer Anwendung der Zugriff auf nicht komprimierte Video Frames gestattet wird.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: MFPROTECTION_VIDEO_FRAMES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350583"
---
# <a name="mfprotection_video_frames-attribute"></a>MF Protection- \_ Video \_ Rahmen Attribut

Gibt an, ob einer Anwendung der Zugriff auf nicht komprimierte Video Frames gestattet wird.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Der Wert 0 gibt an, dass der Anwendung der Zugriff auf die Frames gestattet ist. Dies kann als Ergebnis einer privaten Vereinbarung zwischen der Anwendung und dem jeweiligen verwendeten Inhalts Schutzsystem festgelegt werden.

Der Wert 1 gibt an, dass der Anwendung der Zugriff auf Frames gestattet wird, wenn ein gültiges Anwendungs Zertifikat von der Anwendung bereitgestellt wird (siehe [**imfmediaengineprotectedcontent:: setapplicationcertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

Ein Wert von 0xFFFFFFFF, der der Standardwert ist, bedeutet, dass keinen Anwendungen der Zugriff auf unkomprimierte Frames gestattet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ UWP-apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ UWP-apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




