---
description: Identifiziert die Kombination von Audiogeräten, die die Anwendung derzeit mit dem Voice Capture-DSP verwendet.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973329"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID-Eigenschaft

Identifiziert die Kombination von Audiogeräten, die die Anwendung derzeit mit dem Voice Capture-DSP verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ CLSID

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filtermodus verwenden und der Wert der [MFPKEY \_ WMAAECMA \_ RETRIEVE TS \_ \_ STATS-Eigenschaft](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) VARIANT \_ TRUE ist.

Wenn die [**MFPKEY \_ WMAAECMA \_ RETRIEVE TS \_ \_ STATS-Eigenschaft**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) VARIANT TRUE ist, sammelt der DSP Statistiken zu den Zeitstempeln von den Audiogeräten und speichert diese Informationen in der \_ Registrierung. Diese Statistiken können sich für jede Kombination aus Audioaufnahmegerät und Audiorenderinggerät ändern. Daher muss die Anwendung eine GUID zuweisen, um die bestimmte Kombination von Geräten zu identifizieren, die verwendet werden. Die Anwendung sollte diese GUID nachverfolgen, damit sie dieselbe GUID zuweisen kann, wenn sie das gleiche Audiogerätepaar verwendet.

Wenn Sie den DSP im Quellmodus verwenden, müssen Sie diese Eigenschaft nicht festlegen. Der DSP generiert automatisch eine GUID basierend auf dem Wert der [MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES-Eigenschaft.](mfpkey-wmaaecma-device-indexesproperty.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Voice Capture-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
