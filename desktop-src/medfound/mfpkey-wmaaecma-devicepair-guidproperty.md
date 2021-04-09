---
description: Gibt die Kombination der Audiogeräte an, die von der Anwendung zurzeit mit dem sprach Erfassungs-DSP verwendet werden.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130545"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>Mfpkey \_ wmaaecma \_ devicepair \_ GUID-Eigenschaft

Gibt die Kombination der Audiogeräte an, die von der Anwendung zurzeit mit dem sprach Erfassungs-DSP verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ CLSID

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Filter Modus verwenden und der Wert der Eigenschaft [mfpkey \_ wmaaecma \_ Abruf \_ TS \_ Stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) auf Variant true festgelegt ist \_ .

Wenn die Eigenschaft " [**mfpkey \_ wmaaecma \_ Abruf von \_ TS \_ Stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) " Variant \_ true ist, sammelt der DSP Statistiken zu den Zeitstempeln von den Audiogeräten und speichert diese Informationen in der Registrierung. Diese Statistiken können für jede Kombination aus audioerfassungs-und audiorendering-Gerät geändert werden. Daher muss die Anwendung eine GUID zuweisen, um die jeweilige Kombination von verwendeten Geräten zu identifizieren. Die Anwendung sollte diese GUID nachverfolgen, sodass Sie dieselbe GUID zuweisen kann, wenn Sie dasselbe paar von Audiogeräten verwendet.

Wenn Sie den DSP im Quell Modus verwenden, müssen Sie diese Eigenschaft nicht festlegen. Der DSP generiert automatisch eine GUID basierend auf dem Wert der Eigenschaft [mfpkey \_ wmaaecma- \_ Geräte \_ Indizes](mfpkey-wmaaecma-device-indexesproperty.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
