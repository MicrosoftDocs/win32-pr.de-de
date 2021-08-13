---
description: Wird von der Mediensitzung ausgelöst, wenn sich das Format in einer Mediensenke ändert.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: MESessionStreamSinkFormatChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08d086d5966e0fc1f6ce4b4b3d639b40d795a4e05799f3928f61afa9abddf4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268590"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>MESessionStreamSinkFormatChanged-Ereignis

Wird von der Mediensitzung ausgelöst, wenn sich das Format in einer Mediensenke ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                    | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ MF-EREIGNISAUSGABEKNOTEN \_**](mf-event-output-node-attribute.md)<br/> | Identifiziert den Topologieknoten für die Mediensenke, deren Format geändert wurde.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




