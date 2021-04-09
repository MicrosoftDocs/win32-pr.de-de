---
description: Gibt an, ob der UDP (User Datagram Protocol)-Transport in der Netzwerkquelle aktiviert ist.
ms.assetid: d46a59e6-8abc-484b-aecc-edf57ffff512
title: MFNETSOURCE_ENABLE_UDP-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326cbd375a7d7e22ea2afc121dd4af9086e60c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959046"
---
# <a name="mfnetsource_enable_udp-property"></a>MF-Quell \_ Eigenschaft "UDP aktivieren" \_

Gibt an, ob der UDP (User Datagram Protocol)-Transport in der Netzwerkquelle aktiviert ist.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Boolescher Wert (**Long**)

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ enable \_ UDP** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Unterstützte Protokolle](supported-protocols.md)
</dt> </dl>

 

 




