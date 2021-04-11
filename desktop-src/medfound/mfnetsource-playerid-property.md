---
description: Der Wert des Felds &\# 0034; c-playerid&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: MFNETSOURCE_PLAYERID-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d20754c93057ef3f000fc9c7201cda7ec287eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042640"
---
# <a name="mfnetsource_playerid-property"></a>\_Playerid-Eigenschaft von MF NetSource

Der Wert des Felds "c-playerid", das von der Netzwerkquelle für die Protokollierung verwendet wird. Anwendungen können diese Eigenschaft auf einen beliebigen Zeichen folgen Wert festlegen.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Breit Zeichen-Zeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszval**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ playerid** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

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
</dt> </dl>

 

 




