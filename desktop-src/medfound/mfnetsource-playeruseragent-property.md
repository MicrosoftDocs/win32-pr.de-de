---
description: Der Wert des zweiten Teils des \# Felds &0034; CS (User-Agent) &\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: MFNETSOURCE_PLAYERUSERAGENT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357380"
---
# <a name="mfnetsource_playeruseragent-property"></a>Eigenschaft "playeruseragent" von MF NetSource \_

Der Wert des zweiten Teils des Felds "CS (User-Agent)", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf einen beliebigen Zeichen folgen Wert festlegen.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Breit Zeichen-Zeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszval**



## <a name="remarks"></a>Bemerkungen

Der Konstante **MF-Quell- \_ playeruseragent** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Protokollierung](client-logging.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MF-Quelle \_ browseruseragent**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




