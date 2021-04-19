---
description: Aktiviert den Modus mit niedriger Latenz in einem Codec.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: CODECAPI_AVLowLatencyMode-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346666"
---
# <a name="codecapi_avlowlatencymode-property"></a>Codecapi \_ avlowlatencymode-Eigenschaft

Aktiviert den Modus mit niedriger Latenz in einem Codec.

## <a name="data-type"></a>Datentyp

**ulong** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avlowlatencymode**

## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert ungleich 0 (null) ist, ist der Modus mit niedriger Latenzzeit aktiviert. Wenn der Wert 0 (null) ist, ist der Modus mit niedriger Latenz deaktiviert.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt sowohl für Encoder als auch für Decoders.

Der Modus mit niedriger Latenz ist für Echtzeitkommunikation oder Live Erfassung nützlich, wenn die Latenz minimiert werden sollte. Der Modus mit niedriger Latenz kann jedoch auch die Decodierung oder Codierungsqualität verringern.

Es wird erwartet, dass der Encoder keine Stichproben Verzögerung aufgrund der Neuanordnung von Frames im Codierungsprozess hinzufügt, und ein Eingabe Beispiel erstellt ein Ausgabe Beispiel. B Slices/Frames können vorhanden sein, solange Sie keine Neuanordnung von Frames im Encoder einleiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**Icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

