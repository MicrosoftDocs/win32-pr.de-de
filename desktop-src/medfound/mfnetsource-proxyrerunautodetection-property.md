---
description: Gibt an, ob der Standardproxylocator die automatische Proxyerkennung erzwingen soll.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3351766302952390bbe67ea2d86cd76e93b9267328fe2c07e2656a38b3fd2906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713990"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>MFNETSOURCE \_ PROXYRERUNAUTODETECTION (Eigenschaft)

Gibt an, ob der Standardproxylocator die automatische Proxyerkennung erzwingen soll.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Boolescher Wert (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYSETTINGS** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Proxylocator beim Erstellen des Proxylocatorobjekts zu konfigurieren. Übergeben Sie zum Festlegen der Eigenschaft einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Im Modus für die automatische Erkennung verwendet der Proxylocator den WinInet-Proxyerkennungsmechanismus. Um die automatische Erkennung zu erzwingen, legen Sie den Wert auf 0 fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Proxyunterstützung für Netzwerkquellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




