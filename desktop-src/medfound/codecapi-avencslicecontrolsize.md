---
description: Gibt die Größe des Slice in Einheiten von Megabyte (MB), Bits oder MB an.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127977"
---
# <a name="codecapi_avencslicecontrolsize-property"></a>Codecapi \_ avencslicecontrolsize (Eigenschaft)

Gibt die Größe des Slice in Einheiten von Megabyte (MB), Bits oder MB an.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencslicecontrolsize**

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Die Bedeutung des Werts von codecapi \_ avencslicecontrolsize wird von der [codecapi-Eigenschaft " \_ avencslicecontrolmode](codecapi-avencslicecontrolmode.md) " gesteuert. In der folgenden Tabelle wird veranschaulicht, wie die Eigenschaften codecapi \_ avencslicecontrolsize und codecapi \_ avencslicecontrolmode die Größe und die Anzahl der Slices in einem Frame steuern.



| Codecapi \_ avencslicecontrolmode-Einstellung | Bedeutung des Werts                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                       | Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Makroblocks angibt. <br/> Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblöcke im Frame ist.<br/>                                                                                                                                                                         |
| 1                                       | Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Bits angibt. <br/> Der Encoder sollte einen neuen Slice im Makroblock starten, der bewirkt, dass die Anzahl der Bits im Slice diesen Wert überschreitet (sodass die Größe jedes Slice immer kleiner als oder gleich diesem Wert ist). Dies bedeutet, dass die letzte Slice-Größe erheblich kleiner als dieser Wert sein könnte. <br/> |
| 2                                       | Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Makroblock Zeilen angibt. <br/> Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblock Zeilen im Frame ist.<br/>                                                                                                                                                                 |



 

Wenn die Anwendung keinen Wert für [codecapi \_ avencslicecontrolmode](codecapi-avencslicecontrolmode.md)festgelegt, sollte der Encoder einen Fehler zurückgeben.

Der empfohlene Standardwert ist, dass ein einzelner Slice für den gesamten Frame vorhanden ist.

Einige Encoder können Slices parallel codieren, sodass die Leistung abhängig von den Slice-Steuerelement Einstellungen beeinträchtigt werden kann. Beispielsweise kann das Codieren eines Frames als einzelner Slice langsamer sein, als wenn der Frame als mehrere Slices codiert wurde.

Die Slice-Steuerelement Einstellungen sind dynamisch und können während der Codierungs Sitzung geändert werden.

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

 

 




