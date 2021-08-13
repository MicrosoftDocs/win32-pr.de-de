---
description: Der Wert des Felds \# &0034;cs(Referer)&0034;, das die Netzwerkquelle für \# die Protokollierung verwendet.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6be6d64682f0f8d607e813927059360ff1273a33d87791fb7eab55ff10261e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739035"
---
# <a name="mfnetsource_browserwebpage-property"></a>MFNETSOURCE \_ BROWSERWEBPAGE (Eigenschaft)

Der Wert des Felds "cs(Referer)", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf die URL der Webseite festlegen, in die die Anwendung eingebettet wurde.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

Breitzeichenzeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die Konstante **MFNETSOURCE \_ BROWSERWEBPAGE** definiert die GUID für diesen Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientprotokollierung](client-logging.md)
</dt> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




