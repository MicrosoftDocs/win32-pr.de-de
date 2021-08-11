---
description: Speichert den IUnknown-Zeiger der Klasse, die die BERSSLCertificateManager-Schnittstelle implementiert.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6f853ae3fe44a9c4508386df4096e4adac36f3cec8a8cf199eb91cb87e1fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243294"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER-Eigenschaft

Speichert den **IUnknown-Zeiger** der Klasse, die die [**BERSSLCertificateManager-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) implementiert. Die Client-Implementierung stellt Methoden zum Erhalten des CLIENT-SSL-Zertifikats zur Verfügung, wenn es vom Server angefordert wird.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**IUnknown-Zeiger**

VT \_ UNKNOWN

**beival**



## <a name="remarks"></a>Hinweise

Die **MFNETSOURCE \_ SSLCERTIFICATE \_ MANAGER-Konstante** definiert die GUID für den Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festlegen zu können, übergeben Sie einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




