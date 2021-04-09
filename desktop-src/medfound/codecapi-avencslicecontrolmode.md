---
description: Gibt den Slice-Steuerelement Modus an. Gültige Werte sind 0, 1 und 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958655"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>Codecapi- \_ Eigenschaft "avencslicecontrolmode"

Gibt den Slice-Steuerelement Modus an. Gültige Werte sind 0, 1 und 2.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencslicecontrolmode**

## <a name="property-value"></a>Eigenschaftswert

Werte für Slice-Steuerelement Modus:



| Wert                                                                        | Bedeutung                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Wenn dieser Wert auf 0 festgelegt wird, wird angegeben, dass die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Einheiten von makroblöcken pro Slice angibt.<br/>     |
| <dl> <dt>1</dt> </dl> | Wenn dieser Wert auf 1 festgelegt wird, gibt die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Bits-Einheiten pro Slice an.<br/>            |
| <dl> <dt>2</dt> </dl> | Wenn dieser Wert auf 2 festgelegt wird, gibt die [codecapi-Eigenschaft " \_ avencslicecontrolsize](codecapi-avencslicecontrolsize.md) " die Slice-Größe in Einheiten von Makroblock Zeilen pro Slice an.<br/> |



 

Der Encoder gibt die Werte zurück, die er unterstützt.

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Es wird empfohlen, dass der Encoder " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützt.

Wenn [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) nicht für codecapi \_ avencslicecontrolmode aufgerufen wird, kann [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) für codecapi \_ avencslicecontrolmode den **VFW \_ E \_ codecapi \_ ohne \_ aktuellen \_ Wert** zurückgeben. " [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) " gibt möglicherweise " **VFW \_ E \_ codecapi \_ No \_ default** " für codecapi \_ avencslicecontrolmode zurück.

Der empfohlene Standardwert ist 2 (Größe in MB Zeile pro Slice).

Dabei handelt es sich um eine statische API, was bedeutet, dass sich die Anwendung bei Ausführung des Encoders nicht geändert hat.

## <a name="examples"></a>Beispiele


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

