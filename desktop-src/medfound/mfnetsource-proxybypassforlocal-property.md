---
description: Gibt an, ob der Proxylocator einen Proxyserver für lokale Adressen verwenden soll.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1de60371ac71e570b9c11abcbc255e20efe1793884ebb0746834d32a34353006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954790"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MFNETSOURCE \_ PROXYBYPASSFORLOCAL-Eigenschaft

Gibt an, ob der Proxylocator einen Proxyserver für lokale Adressen verwenden soll.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um den Proxylocator beim Erstellen des Proxylocatorobjekts zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** im *pProxyConfig-Parameter* der [**MFCreateProxyLocator-Funktion.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) Der Wert muss auf 0 festgelegt werden, wenn der Proxyserver für lokale Adressen verwendet werden soll. Andernfalls wird der Standardproxylocator durch einen Wert ungleich 0 (null) so konfiguriert, dass der Proxyserver für lokale Adressen übersprungen wird.

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

 

 




