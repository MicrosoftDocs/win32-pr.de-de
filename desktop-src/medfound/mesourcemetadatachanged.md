---
description: Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: MESourceMetadataChanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959052"
---
# <a name="mesourcemetadatachanged-event"></a>MESourceMetadataChanged-Ereignis

Wird von einer Medienquelle ausgelöst, wenn die Metadaten aktualisiert werden.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn die Medienquelle nicht alle Metadaten bereitstellen kann, wenn die Quelle erstmalig erstellt wird, sollte dieses Ereignis ausgelöst werden, nachdem die Metadaten verfügbar sind.

Von der Medienquelle sollte ein neuer Präsentations Deskriptor erstellt werden, und alle Attribute aus dem Präsentations Deskriptor (PD) werden in das Ereignis Objekt kopiert. Die Anwendung kann das Ereignis Objekt zum Auflisten der neuen PD-Attribute verwenden. Insbesondere sind die Werte für die Dateigröße von [MF \_ PD \_ ](mf-pd-duration-attribute.md) und die [ \_ \_ gesamte \_ Datei \_ Größe von MF PD](mf-pd-total-file-size-attribute.md) möglicherweise unbekannt, bis die Datei vollständig heruntergeladen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Präsentations deskriptorattribute](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




