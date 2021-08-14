---
description: Gibt an, welche Audiogeräte der Voice Capture-DSP zum Erfassen und Rendern von Audio verwendet.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e9fd9eae8d53f1fa19bd8b55d94d292b9cd6cbf214b7a71a6473f1af647f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872991"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES-Eigenschaft

Gibt an, welche Audiogeräte der Voice Capture-DSP zum Erfassen und Rendern von Audio verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

(-1, -1).

## <a name="applies-to"></a>Gilt für

-   [Voice Capture-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Quellmodus verwenden. Der DSP ignoriert diese Eigenschaft im Filtermodus.

Der Wert der -Eigenschaft ist zwei 16-Bit-WORD-s, die in ein **DWORD gepackt sind.** Die oberen 16 Bits geben das Audiorenderinggerät an (in der Regel ein Lautsprecher), und die unteren 16 Bits geben das Erfassungsgerät an (in der Regel ein Mikrofon). Jedes Gerät wird als Index in der Audiogerätesammlung angegeben. Wenn der Index -1 ist, wird das Standardgerät verwendet.

Der Geräteindex entspricht dem Sammlungsindex, der in der [**IMMDeviceCollection-Schnittstelle verwendet**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) wird. Die Anwendung muss die Far-End-Stimme über das ausgewählte Renderinggerät wieder geben. (Die Far-End-Stimme ist die Stimme der Person am anderen Ende der Telefonleitung, die über den Lautsprecher auf dem Computer des Benutzers abgespielt wird.) Wenn das ausgewählte Renderinggerät über keinen aktiven Stream verfügt, kann der DSP keine Ausgabe verarbeiten.

Der Standardwert dieser Eigenschaft ist (-1, -1).

Das folgende Beispiel zeigt, wie die **PROPVARIANT** für diese Eigenschaft initialisiert wird.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



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

 

 
