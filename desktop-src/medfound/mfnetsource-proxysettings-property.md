---
description: Gibt die Konfigurationseinstellung für den Standardproxylocator an.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: MFNETSOURCE_PROXYSETTINGS -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6af82b593899eb504818ff041c6c6839c4cca1b18ea29218f7259c41b4df9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738675"
---
# <a name="mfnetsource_proxysettings-property"></a>MFNETSOURCE \_ PROXYSETTINGS(Eigenschaft)

Gibt die Konfigurationseinstellung für den Standardproxylocator an. Der Wert dieser Eigenschaft ist ein Member der [**MFNET \_ PROXYSETTINGS-Enumeration.**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings)



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYSETTINGS** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Proxylocator beim Erstellen des Standardproxylocatorobjekts zu konfigurieren. Übergeben Sie zum Festlegen der Eigenschaft einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator)

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

 

 




