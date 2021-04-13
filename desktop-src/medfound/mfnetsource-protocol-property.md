---
description: Gibt das Steuerungs Protokoll an, das von der Netzwerkquelle verwendet wird.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525979"
---
# <a name="mfnetsource_protocol-property"></a>MF-Quell \_ Protokoll Eigenschaft

Gibt das Steuerungs Protokoll an, das von der Netzwerkquelle verwendet wird. Der Wert dieser Eigenschaft ist ein Member der Enumeration des [**mfnetsource- \_ Protokoll \_ Typs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**LONG**

VT \_ I4

**LVAL**



## <a name="remarks"></a>Bemerkungen

Das Konstante **MF-Quell \_ Protokoll** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

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

 

 




