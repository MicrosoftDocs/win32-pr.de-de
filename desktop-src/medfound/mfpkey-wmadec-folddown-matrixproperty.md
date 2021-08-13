---
description: Gibt die vom Autor bereitgestellten Fold-Down-Koeffizienten für die Decodierung von Multichannelaudio für weniger Kanäle an, als der codierte Stream enthält.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1b9eb1259c2a8c23f7b993699e1c51f17c09636afd7d19de23ce033fd269fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463160"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>MFPKEY \_ WKYC \_ FOLDDOWN \_ MATRIX-Eigenschaft

Gibt die vom Autor bereitgestellten Fold-Down-Koeffizienten für die Decodierung von Multichannelaudio für weniger Kanäle an, als der codierte Stream enthält.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Datentyp

**VT \_ ARRAY \| VT \_ I4**

## <a name="remarks"></a>Hinweise

Ein Audiodecoder kann als DirectX Media Object (DMO) oder als Media Foundation Transform (MFT) fungieren. Informationen dazu, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codecverweisseiten unter [Codec-Objekte.](codecobjects.md)

Wenn Sie einen Decoder als DMO verwenden, kann der Decoder ein Kanalfalout ausführen, und Sie können heruntergefahrene Ausgabemedientypen aufzählen, indem Sie [**IMediaObject::GetOutputType aufrufen.**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)

Wenn Sie einen Decoder als MFT verwenden, führt der Decoder standardmäßig kein Fold down aus und bietet keine heruntergefahrenen Ausgabemedientypen. Ein Decoder, der als MFT verwendet wird, führt nur dann ein Folddown aus, wenn benutzerdefinierte Folddownkoeffizienten mithilfe der **\_ MFPKEY WMULTIC \_ FOLDDOWN \_ MATRIX-Eigenschaft festgelegt** werden.

Wenn die **MFPKEY \_ WKYC \_ FOLDDOWN \_ MATRIX-Eigenschaft** nicht für den Audiodecoder MFT festgelegt ist und Sie ein Folddown ausführen möchten, können Sie (als MFT) den digitalen Signalprozessor Audio Resampler verwenden.

Der Wert für diese Eigenschaft ist eine Zeichenfolge, die fold-down-Koeffizienten in einer durch Komma getrennten Liste von ganzzahligen Werten enthält. Die Liste muss eine Reihe von ganzen Zahlen für jeden Kanal im codierten Inhalt enthalten, der der Anzahl der Kanäle im decodierten Inhalt entspricht.

Wenn der Koeffizient 0 (null) ist, muss der in der Zeichenfolge zu verwendende Wert "-2147483648" sein. Andernfalls wird der Wert mit der Gleichung 20 \* 65536 \* log10(x) berechnet.

Koeffizienten werden in der Reihenfolge der Kanalmasken aufgeführt, wie durch die in der Headerdatei mmreg.h enthaltenen Kanalmaskenkonst constants definiert. Daher stellen die ersten beiden Werte in einem 6-zu-2-Kanal-Fold-Down die Teile des linken Ausgabekanals und des rechten Ausgabekanals dar, die aus dem linken Mittelkanal im 6-Kanal-Stream bilden.

Sie sollten diese Eigenschaft nur festlegen, wenn vom Autor bereitgestellte Fold-Down-Werte mit dem codierten Inhalt beibehalten werden. Andernfalls lassen Sie den Decoder eigene Berechnungen durchführen.

Der Windows Media Audio 10 Professional codec unterstützt derzeit nur das Herunterklappen auf zwei Kanäle.

Wenn die [MFPKEY \_ WRECC \_ SPKRCFG-Eigenschaft](mfpkey-wmadec-spkrcfgproperty.md) auf **DSSPEAKER \_ SURROUND** festgelegt ist, ignoriert der Codec vom Autor bereitgestellte Fold-Down-Koeffizienten und bildet ein 2-Kanal-Signal, das vom Matrixdecoder des Empfängers verarbeitet werden kann. Auf diese Weise können umschließender Geräte vier Kanäle liefern. Dieser Modus wird nur unterstützt, wenn die Quelle 5.1 ist. Der Codec kann nur 8 Kanäle auf zwei Kanäle umklappen.

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

 

 
