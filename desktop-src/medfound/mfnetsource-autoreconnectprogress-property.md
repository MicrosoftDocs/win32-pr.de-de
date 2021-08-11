---
description: Gibt an, wie oft die Netzwerkquelle versucht hat, erneut eine Verbindung mit dem Netzwerk herzustellen.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: MFNETSOURCE_AUTORECONNECTPROGRESS-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cfbf0bac147b3608145d3ef38eb328a44de1c064899a5e7800acbadfadcf709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243874"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>MFNETSOURCE \_ AUTORECONNECTPROGRESS-Eigenschaft

Gibt an, wie oft die Netzwerkquelle versucht hat, erneut eine Verbindung mit dem Netzwerk herzustellen.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**DWORD** (gespeichert als **LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

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

[Netzwerkquellfeatures](network-source-features.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




