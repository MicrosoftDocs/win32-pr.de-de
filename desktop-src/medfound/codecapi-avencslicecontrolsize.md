---
description: Gibt die Größe des Slices in Mb-, Bit- oder MB-Zeileneinheiten an.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d068d8b2c5fc15fdb82c3ffe068e6926d28228a19367114067e02ebc44b03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035348"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>CODECAPI \_ AVEncSliceControlSize-Eigenschaft

Gibt die Größe des Slices in Mb-, Bit- oder MB-Zeileneinheiten an.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncSliceControlSize**

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Die Bedeutung des Werts von CODECAPI \_ AVEncSliceControlSize wird durch die [CODECAPI \_ AVEncSliceControlMode-Eigenschaft](codecapi-avencslicecontrolmode.md) gesteuert. Die folgende Tabelle veranschaulicht, wie die Eigenschaften CODECAPI \_ AVEncSliceControlSize und CODECAPI \_ AVEncSliceControlMode die Größe und Anzahl von Slices in einem Frame steuern.



| \_CODECAPI AVEncSliceControlMode-Einstellung | Bedeutung des Werts                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Dies ist eine ganze Zahl, die die Größe jedes Slices im Frame in Einheiten von Makroblocks angibt. <br/> Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblocks im Frame ist.<br/>                                                                                                                                                                         |
| 1                                       | Dies ist eine ganze Zahl, die die Größe jedes Slices im Frame in Biteinheiten angibt. <br/> Der Encoder sollte einen neuen Slice am Makroblock starten, der bewirkt, dass die Anzahl der Bits im Slice diesen Wert überschreitet (sodass die Größe jedes Slices immer kleiner oder gleich diesem Wert ist). Dies bedeutet, dass die Größe des letzten Slices deutlich kleiner als dieser Wert sein kann. <br/> |
| 2                                       | Dies ist eine ganze Zahl, die die Größe jedes Slices im Frame in Einheiten von Makroblockzeilen angibt. <br/> Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblockzeilen im Frame ist.<br/>                                                                                                                                                                 |



 

Wenn die Anwendung keinen Wert für [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)festgelegt, sollte der Encoder einen Fehler zurückgeben.

Die empfohlene Standardeinstellung ist ein einzelner Slice für den gesamten Frame.

Einige Encoder codieren Slices möglicherweise parallel, sodass die Leistung abhängig von den Einstellungen des Slicesteuerelements beeinträchtigt werden kann. Beispielsweise kann die Codierung eines Frames als einzelner Slice langsamer sein, als wenn der Frame als mehrere Slices codiert wurde.

Die Slicesteuerelementeinstellungen sind dynamisch und können während der Codierungssitzung geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




