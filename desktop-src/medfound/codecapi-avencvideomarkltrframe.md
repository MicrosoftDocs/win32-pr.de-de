---
description: Markiert den aktuellen Frame als einen Ltr-Frame.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524627"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>Codecapi \_ avencvideomarkltrframe (Eigenschaft)

Markiert den aktuellen Frame als einen Ltr-Frame.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideomarkltrframe**

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Der Wert dieses Steuer Elements ist der Wert der H. 264-Syntax *longtermframittelx* , die dem aktuellen Frame zugeordnet ist. Wenn sich der aktuelle Frame nicht in der Basisschicht befindet, z. b. wenn die *Temporale \_ ID* des Syntax Elements nicht gleich 0 ist, gilt diese Eigenschaft für den nächsten Basisschicht Rahmen in der Codierungs Reihenfolge.

Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zum Markieren eines Ltr-Frames mithilfe der codecapi- \_ Eigenschaft "avencvideomarkltrframe" ausgegeben wurde und der Encoder einen Frame noch nicht als Ltr gekennzeichnet hat. Mit anderen Worten, der Encoder sollte codecapi- \_ krecvideomarkltrframe-Anforderungen nicht in die Warteschlange stellen. Wenn eine codecapi-Anforderung für den Vorgang " \_ avencvideomarkltrframe" übermittelt wird, während eine andere codecapi-Datei " \_ avencvideomarkltrframe" noch aussteht, sollte die ältere Anforderung gelöscht werden.

Die Eigenschaft "codecapi \_ avencvideomarkltrframe" ist dynamisch und kann während der Codierungs Sitzung festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




