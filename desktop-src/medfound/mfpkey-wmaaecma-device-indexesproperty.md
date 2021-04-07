---
description: Gibt an, welche Audiogeräte der sprach Erfassungs-DSP zum Erfassen und Rendern von Audiodaten verwendet.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863439"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Mfpkey \_ wmaaecma- \_ Geräte \_ Index Eigenschaft

Gibt an, welche Audiogeräte der sprach Erfassungs-DSP zum Erfassen und Rendern von Audiodaten verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

(-1,-1).

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, wenn Sie den DSP im Quell Modus verwenden. Der DSP ignoriert diese Eigenschaft im Filter Modus.

Der Wert der-Eigenschaft ist 2 16-Bit- **Wörter**, die in ein **DWORD** gepackt werden. In den oberen 16 Bits ist das audiorenderinggerät (in der Regel ein Redner) angegeben, und die unteren 16 Bits geben das Erfassungsgerät (in der Regel ein Mikrofon) an. Jedes Gerät wird als Index in der audiogeräteauflistung angegeben. Wenn der Index-1 ist, wird das Standardgerät verwendet.

Der Geräte Index entspricht dem Sammlungs Index, der in der [**immendvicecollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) -Schnittstelle verwendet wird. Die Anwendung muss die ganz gängige Stimme über das ausgewählte renderinggerät abspielen. (Die vielseitige Stimme ist die Stimme der Person am anderen Ende der Telefonleitung, die über den Sprecher auf dem Computer des Benutzers gespielt wird.) Wenn das ausgewählte renderinggerät keinen aktiven Stream hat, kann der DSP keine Ausgabe verarbeiten.

Der Standardwert dieser Eigenschaft ist (-1,-1).

Im folgenden Beispiel wird gezeigt, wie die **PROPVARIANT** für diese Eigenschaft initialisiert wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
