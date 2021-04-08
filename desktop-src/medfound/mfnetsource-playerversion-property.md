---
description: Der Wert des Felds &\# 0034; c-Playerversion&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759667"
---
# <a name="mfnetsource_playerversion-property"></a>Eigenschaft "Playerversion" von MF NetSource \_

Der Wert des Felds "c-Playerversion", das von der Netzwerkquelle für die Protokollierung verwendet wird. Anwendungen können diese Eigenschaft auf die Versionsnummer der Anwendung festlegen.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**LONGLONG**

VT \_ I8

**Hval**



## <a name="remarks"></a>Bemerkungen

Die Konstante **MF-Quelle \_ Playerversion** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [quellresolver](source-resolver.md).

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

 

 




