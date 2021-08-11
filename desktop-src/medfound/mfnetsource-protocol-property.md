---
description: Gibt das von der Netzwerkquelle verwendete Steuerungsprotokoll an.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae15ce40e7c049552cbb0f4916f5f4ff70ef6e55746528ebe0083eee69b22a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243322"
---
# <a name="mfnetsource_protocol-property"></a>MFNETSOURCE \_ PROTOCOL-Eigenschaft

Gibt das von der Netzwerkquelle verwendete Steuerungsprotokoll an. Der Wert dieser Eigenschaft ist ein Member der [**MFNETSOURCE \_ PROTOCOL \_ TYPE-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type)



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROTOCOL** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um diese Eigenschaft abzurufen, fragen Sie die Netzwerkquelle nach der **IPropertyStore-Schnittstelle** ab, und rufen **Sie IPropertyStore::GetValue auf.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Unterstützte Protokolle](supported-protocols.md)
</dt> </dl>

 

 




