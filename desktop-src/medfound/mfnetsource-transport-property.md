---
description: Gibt das Transportprotokoll an, das von der Netzwerkquelle verwendet wird.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863156"
---
# <a name="mfnetsource_transport-property"></a>MF-Quell- \_ Transport Eigenschaft

Gibt das Transportprotokoll an, das von der Netzwerkquelle verwendet wird. Der Wert dieser Eigenschaft ist ein Member der [**mfnetsource- \_ \_ Transporttyp**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) -Enumeration.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**LONG**

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Der Konstante **MF-Quell \_ Transport** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um diese Eigenschaft abzurufen, Fragen Sie die Netzwerkquelle nach der **IPropertyStore** -Schnittstelle ab, und rufen Sie **IPropertyStore:: GetValue** auf.

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

 

 




