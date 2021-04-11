---
description: Wird ausgelöst, wenn eine Medien Senke ungültig wird.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Mesinkinvalivali-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214778"
---
# <a name="mesinkinvalidated-event"></a>Mesinkinvalivalidereignis

Wird ausgelöst, wenn eine Medien Senke ungültig wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                    | BESCHREIBUNG                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**MF- \_ Ereignis \_ Ausgabe \_ Knoten**](mf-event-output-node-attribute.md)<br/> | Identifiziert den topologieknoten für diese Medien Senke.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Medien Sitzung löst dieses Ereignis aus, wenn eines der folgenden Ereignisse von der Medien Senke empfangen wird:

-   [Meaudiosessiondeviceremoved](meaudiosessiondeviceremoved.md)

-   [Meaudiosessiontrennt](meaudiosessiondisconnected.md)

-   [Meaudiosessionexclusivemodeoverride](meaudiosessionexclusivemodeoverride.md)

-   [Meaudiosessionformatchanged](meaudiosessionformatchanged.md)

-   [Meaudiosessionservershutdown](meaudiosessionservershutdown.md)

Eine Medien Senke kann dieses Ereignis auch erhöhen. in diesem Fall legt die Medien Sitzung das Attribut " [**MF \_ Event \_ Output \_ Node**](mf-event-output-node-attribute.md) " für das Ereignis fest und leitet das Ereignis an die Anwendung weiter.

Wenn die Anwendung dieses Ereignis empfängt, muss Sie die Medien Senke neu erstellen und die Topologie erneut in die Warteschlange stellen.

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

 

 




