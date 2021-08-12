---
description: Der Wert des zweiten Teils des &\# Felds 0034;cs(User-Agent)&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: MFNETSOURCE_PLAYERUSERAGENT-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b431780345c8b297bf154813a9713b5b158ecc99cc4384294ee983b8066ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243422"
---
# <a name="mfnetsource_playeruseragent-property"></a>MFNETSOURCE \_ PLAYERUSERAGENT-Eigenschaft

Der Wert des zweiten Teils des Felds "cs(User-Agent)", der von der Netzwerkquelle für die Protokollierung verwendet wird. Anwendungen können diese Eigenschaft auf einen beliebigen Zeichenfolgenwert festlegen.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ PLAYERUSERAGENT** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientprotokollierung](client-logging.md)
</dt> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[**MFNETSOURCE \_ BROWSERUSERAGENT**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




