---
description: Der Medienstrom verwendet dieses Ereignis, um Schutzsystem spezifische Metadaten an den Decoder zu senden.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Mecontentschutzmetadata-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863179"
---
# <a name="mecontentprotectionmetadata-event"></a>Mecontentschutzmetadata-Ereignis

Der Medienstrom verwendet dieses Ereignis, um Schutzsystem spezifische Metadaten an den Decoder zu senden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                              | BESCHREIBUNG                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [\_ \_ \_ \_ Schlüsseldaten für den MF-Ereignisdaten Strom](mf-event-stream-metadata-keydata.md)<br/>                | Dies ist ein optionales Attribut. Spezifische Daten des Schutzsystems.<br/> <br/>              |
| [Daten \_ \_ Strom- \_ Schlüssel \_ - \_ IDs des MF-Ereignisdaten Stroms](mf-event-stream-metadata-content-keyids.md)<br/> | Inhalts Schlüssel-IDs, denen das Ereignis zugeordnet ist.<br/> <br/>                          |
| [MF- \_ Ereignisdaten \_ Strom Metadaten-System \_ \_ Mid](mf-event-stream-metadata-systemid.md)<br/>              | Dies ist ein optionales Attribut. Die System-ID, für die die Schlüsseldaten vorgesehen sind.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird z. b. zum kommunizieren eines Schlüssel Rotations Ereignisses verwendet. In diesem Fall sollte Sie so früh wie möglich gesendet werden, um dem Decoder Zeit zu geben, sich selbst vorzubereiten, bevor mit der neuen Schlüssel-ID verschlüsselte Beispiele gestartet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




