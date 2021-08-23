---
description: Gibt den Hostnamen des Proxyservers an.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663670"
---
# <a name="mfnetsource_proxyhostname-property"></a>MFNETSOURCE-Eigenschaft \_ "PROXYHOSTNAME"

Gibt den Hostnamen des Proxyservers an.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYHOSTNAME** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Standardproxylocator beim Erstellen des Proxylocatorobjekts zu konfigurieren. Übergeben Sie zum Festlegen der Eigenschaft einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Diese Eigenschaft muss von der Anwendung festgelegt werden, wenn der Proxylocator für den Betrieb im manuellen Modus konfiguriert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Proxyunterstützung für Netzwerkquellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




