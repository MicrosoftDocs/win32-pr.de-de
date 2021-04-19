---
description: Gibt den Typ der sprach Aktivitäts Erkennung an, den der sprach Erfassungs-DSP ausführt.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: MFPKEY_WMAAECMA_FEATR_VAD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348489"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a>Mfpkey \_ wmaaecma \_ featr \_ VAD (Eigenschaft)

Gibt den Typ der sprach Aktivitäts Erkennung an, den der sprach Erfassungs-DSP ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist ein Member der [AEC \_ VAD- \_ Modus](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) -Enumeration. Die Ausgabe der sprach Aktivitäts Erkennung ist eine Zahl zwischen 0 und 3, die für jeden audioframe berechnet wird. Der DSP codiert das Ergebnis auf das niedrigste Bit der ersten beiden Audiobeispiele in jedem audioframe. Die Bedeutung des Werts hängt vom angegebenen Modus ab.

Der folgende Code zeigt, wie die Ergebnisse aus den Audiodaten extrahiert werden. In diesem Beispiel ist *poutput* ein Zeiger auf den Anfang eines Audioframes in den Ausgabedaten.


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



Der Standardwert dieser Eigenschaft ist 0 (deaktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
