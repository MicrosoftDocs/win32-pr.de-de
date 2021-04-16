---
description: Gibt an, welche Streams erfolgreich mit einer Medien Senke verbunden wurden.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults-Eigenschaft (MF Play. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343928"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>MFP \_ pkey \_ streamrenderingresults (Eigenschaft)

> [!IMPORTANT]
> Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden. Anwendungen sollten die [Medien Sitzung](media-session.md) für die Wiedergabe verwenden.

 

Gibt an, welche Streams erfolgreich mit einer Medien Senke verbunden wurden.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Array von **DWORD** -Werten (**CAUL**)

VT \_ Vector \| VT \_ UI4

**CAUL**



## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann mit dem **MFP- \_ \_ Ereignistyp \_ mediaitem \_ Set** Event gesendet werden.

Der Wert der Eigenschaft ist ein Array von **HRESULT** s. Die Array Einträge entsprechen Streams auf dem aktuellen Medien Element. Jeder Eintrag im Array gibt wie folgt an, ob der entsprechende Stream mit einer Medien Senke verbunden war:

-   Wenn der Stream mit einer Medien Senke verbunden ist, ist der Wert **S \_ OK**.
-   Wenn der Stream nicht ausgewählt ist, ist der Wert **S \_ false**.
-   Wenn beim Versuch, eine Verbindung mit dem Stream herzustellen, ein Fehler aufgetreten ist, ist der Wert ein Fehlercode.

Wenn mindestens ein Stream erfolgreich verbunden wurde, kann die Wiedergabe durchgeführt werden. Der Benutzer kann z. b. den Codec zum Wiedergeben des Audiostreams benötigen, aber nicht den Videostream abspielen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>"MF Play. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**MFP- \_ mediaitem- \_ Set- \_ Ereignis**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




