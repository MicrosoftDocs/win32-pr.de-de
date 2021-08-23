---
description: Gibt das von der Netzwerkquelle verwendete Transportprotokoll an.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933c4051cd3d008082c3b7811fcd88f8b118e51a9e864d947750813c11883b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663470"
---
# <a name="mfnetsource_transport-property"></a>MFNETSOURCE \_ TRANSPORT-Eigenschaft

Gibt das von der Netzwerkquelle verwendete Transportprotokoll an. Der Wert dieser Eigenschaft ist ein Member der [**MFNETSOURCE \_ TRANSPORT \_ TYPE-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ TRANSPORT** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

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

 

 




