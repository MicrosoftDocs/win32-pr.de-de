---
description: Speichert den Hostnamen und den Port des Proxyservers, der von der Netzwerkquelle verwendet wird.
ms.assetid: 164f8ac3-08ce-40a8-ac8d-4c2a267d9db5
title: MFNETSOURCE_PROXYINFO-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0dc9c130045431ce1c460dadd0a3fde5b0eaa6af41c599d8947668d0ae6bfbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690710"
---
# <a name="mfnetsource_proxyinfo-property"></a>MFNETSOURCE \_ PROXYINFO-Eigenschaft

Speichert den Hostnamen und den Port des Proxyservers, der von der Netzwerkquelle verwendet wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYINFO** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Diese Eigenschaft ist schreibgeschützt. Um den Eigenschaftswert aus der Netzwerkquelle abzurufen, rufen **Sie IPropertyStore::GetValue** auf, und übergeben Sie die **PROPERTYKEY-Struktur** im *Schlüsselparameter.* Der **fmtid-Member** von **PROPERTYKEY** muss auf die Eigenschaften-GUID festgelegt werden.

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

[Proxyunterstützung für Netzwerkquellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




