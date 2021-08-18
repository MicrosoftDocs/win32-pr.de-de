---
description: Die PKEY \_ \_ Device DeviceDesc-Eigenschaft enthält die Gerätebeschreibung des Endpunktgeräts (z.B. &\# 0034; Lautsprecher&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c5772029f6c99a86c330f05e3cae3b343e3ee25f39eae4c8d5900e7bf947c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077464"
---
# <a name="pkey_device_devicedesc"></a>PKEY \_ Device \_ DeviceDesc

Die **PKEY \_ Device \_ DeviceDesc-Eigenschaft** enthält die Gerätebeschreibung des Endpunktgeräts (z.B. "Lautsprecher").

Der **vt-Member** der **PROPVARIANT-Struktur** ist auf VT \_ LPWSTR festgelegt.

Der **pwszVal-Member** der **PROPVARIANT-Struktur** zeigt auf eine auf NULL endende Zeichenfolge mit Breitzeichen, die die Gerätebeschreibung enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> <dt>

[Geräteeigenschaften](device-properties.md)
</dt> </dl>

 

 




