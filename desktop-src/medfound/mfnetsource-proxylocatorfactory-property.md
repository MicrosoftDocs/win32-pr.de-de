---
description: Enthält einen Zeiger auf die BENUTZEROBERFLÄCHENetProxyLocatorFactory-Schnittstelle.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc06f58fc11e4d0dcff95274170a76b25160b584231bd2c9e39ed1949b1363e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954740"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>MFNETSOURCE \_ PROXYLOCATORFACTORY-Eigenschaft

Enthält einen Zeiger auf die [**BENUTZEROBERFLÄCHENetProxyLocatorFactory-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory)



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**IUnknown-Zeiger**

VT \_ UNKNOWN

**beival**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PROXYLOCATORFACTORY** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um einen benutzerdefinierten Proxylocator für die Netzwerkquelle zur Verfügung zu stellen. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

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

 

 




