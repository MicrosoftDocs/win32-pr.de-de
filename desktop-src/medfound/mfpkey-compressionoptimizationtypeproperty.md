---
description: Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den Windows Media Video 9 Advanced Profile-Encoder verwendet werden.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471726"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft

Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den Windows Media Video 9 Advanced Profile-Encoder verwendet werden.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft bietet eine schnelle Möglichkeit, eine Reihe von Videocodierungsoptionen zu konfigurieren. Sie kann auf einen der folgenden Werte festgelegt werden.




| Wert | BESCHREIBUNG | 
|-------|-------------|
| 0 | Der Codec erzwingen keine Optimierung und verwendet alle Features, die von anderen Eigenschaften angegeben werden. In vielen Fällen verwendet der Codec interne Logik, um Einstellungen zu bestimmen, wenn sie nicht angegeben sind. Dies ist der Standardwert. | 
| 1 | Aktiviert die Features, die die beste visuelle Qualität erzeugen. Wenn Sie diesen Wert verwenden, wird der Codec so konfiguriert, als ob Sie die folgenden Eigenschaften festgelegt hätten:<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Wenn Sie eine der Eigenschaften in der vorherigen Liste festlegen, überschreibt der wert, den Sie festlegen, die Werte, die dieser Einstellung zugeordnet sind, mit Ausnahme <a href="mfpkey-complexityexproperty.md">von MFPKEY_COMPLEXITYEX.</a><br /> | 




 

Wenn Sie den Wert der MFPKEY COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft auf 1 festlegen, wird auch die Registrierungseinstellung Dquant Option auf 2 und die Registrierungseinstellung Motion Vector Cost Method auf \_ 1 festgelegt. Weitere Informationen finden Sie im Webartikel [Using the Advanced Einstellungen of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




