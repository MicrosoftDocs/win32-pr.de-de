---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215527"
---
# <a name="mfpkey_complexity-property"></a>Mfpkey- \_ Komplexitäts Eigenschaft

\[[**Mfpkey \_ Die Komplexität**](mfpkey-complexityexproperty.md) ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen **mfpkey \_ complexityex**.\]

Gibt die Komplexität des Codierungs Algorithmus an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvccomplexitymode

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt von der Version des Video Encoders ab, wie in der folgenden Tabelle dargestellt.



| Codierungs Version                 | Standardwert |
|---------------------------------|---------------|
| Windows Media Video 9-Encoder   | 3             |
| Windows Media Video 7/8-Encoder | 1             |



 

## <a name="remarks"></a>Bemerkungen

Dieser ganzzahlige Wert liegt zwischen 0 und 3. Niedrigere Werte bewirken, dass der Codec weniger komplizierte Codierungs Algorithmen verwendet. Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität verursachen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.

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

 

 




