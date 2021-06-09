---
description: Aktiviert den Modus mit geringer Latenz in einem Codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826904"
---
# <a name="codecapi_avlowlatencymode-property"></a>\_CODECAPI-Eigenschaft "AVLowLatencyMode"

Aktiviert den Modus mit geringer Latenz in einem Codec.

## <a name="data-type"></a>Datentyp

**ULONG** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVLowLatencyMode**

## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert ungleich 0 (null) ist, wird der Modus mit geringer Latenz aktiviert. Wenn der Wert 0 (null) ist, wird der Modus mit geringer Latenz deaktiviert.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt sowohl für Encoder als auch für Decoder.

Der Modus mit geringer Latenz ist für die Echtzeitkommunikation oder Liveerfassung nützlich, wenn die Latenz minimiert werden soll. Der Modus mit geringer Latenz kann jedoch auch die Decodierungs- oder Codierungsqualität verringern.

Es wird erwartet, dass der Encoder keine Beispielverzögerung aufgrund einer Frame-Neuanordnung im Codierungsprozess hinzufüge, und ein Eingabebeispiel sollte ein Ausgabebeispiel erzeugen. B-Slices/Frames können vorhanden sein, solange sie keine Frame-Neubestellung im Encoder einführen.

> [!WARNING] 
> In der aktuellen Implementierung verwendet der Media Foundation H.264-Decoder den VT_UI4 **für** diese Eigenschaft. Alle anderen Implementierungen, einschließlich des H.264-Encoders, verwenden den Typ **VT_BOOL.**

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | UWP-Apps für Windows Server \[ 2012-Desktop-Apps \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

