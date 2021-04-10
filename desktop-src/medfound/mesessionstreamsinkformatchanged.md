---
description: Wird von der Medien Sitzung ausgelöst, wenn sich das Format in einer Medien Senke ändert.
ms.assetid: f56419f8-7f50-4eda-bf4a-fcdbbe46e180
title: Mesessionstreamsinkformatchanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed59b9600cbaf8cb942a42beb6bed46d62fc15f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215163"
---
# <a name="mesessionstreamsinkformatchanged-event"></a>Mesessionstreamsinkformatchanged-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn sich das Format in einer Medien Senke ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                    | BESCHREIBUNG                                                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**MF- \_ Ereignis \_ Ausgabe \_ Knoten**](mf-event-output-node-attribute.md)<br/> | Identifiziert den topologieknoten für die Medien Senke, deren Format geändert wurde.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




