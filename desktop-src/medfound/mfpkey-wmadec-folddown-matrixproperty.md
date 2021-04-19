---
description: Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356848"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>Eigenschaft "mfpkey \_ wmadec- \_ FoldDown- \_ Matrix"

Gibt die vom Autor bereitgestellten Fold-Koeffizienten für das Decodieren von Multichannel-Audiodaten für weniger Kanäle an, als der codierte Stream enthält.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacfolddownxychannels

g \_ wszwmacfoldxychannelsz

## <a name="data-type"></a>Datentyp

**VT \_ array \| VT \_ I4**

## <a name="remarks"></a>Bemerkungen

Ein Audiodecoder kann als DirectX-Medienobjekt (DMO) oder als Media Foundation Transformation (MFT) fungieren. Informationen darüber, wann ein Decoder als DMO oder MFT fungiert, finden Sie auf den einzelnen Codec-Referenzseiten unter [Codec-Objekte](codecobjects.md).

Wenn Sie einen Decoder als DMO verwenden, kann der Decoder den Kanal durchlaufen, und Sie können durch Aufrufen von [**imediaobject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)Ausgabemedien Typen aufklappen.

Wenn Sie einen Decoder als MFT verwenden, führt der Decoder standardmäßig keine abklappvorgänge aus und bietet keine Ausgabemedien Typen mit einem Fold-Vorgang. Ein Decoder, der als MFT fungiert, führt die Faltung nur dann durch, wenn benutzerdefinierte Fold-Koeffizienten mithilfe der Eigenschaft **mfpkey \_ wmadec- \_ FoldDown- \_ Matrix** festgelegt werden.

Wenn die **mfpkey \_ wmadec- \_ \_ Matrix** Eigenschaft nicht auf dem Audiodecoder-MFT festgelegt ist und Sie ein Fold ausführen möchten, können Sie (als MFT) den audioresampler Digital Signal Processor verwenden.

Der Wert für diese Eigenschaft ist eine Zeichenfolge, die in einer durch Trennzeichen getrennten Liste von ganzzahligen Werten in einer durch Trennzeichen getrennten Liste mit separaten Werten. Die Liste muss eine Reihe von ganzen Zahlen für jeden Kanal im codierten Inhalt enthalten, der der Anzahl der Kanäle im decodierten Inhalt entspricht.

Wenn der Koeffizient NULL ist, muss der Wert, der in der Zeichenfolge verwendet werden soll, "-2147483648" lauten; andernfalls wird der Wert mit der Gleichung berechnet: 20 \* 65536 \* log10 (x).

Koeffizienten werden in der Reihenfolge der Kanalmasken aufgeführt, wie von den channelmasken Konstanten definiert, die in der Header Datei "mmreg. h" enthalten sind. Daher stellen die ersten beiden Werte in einer 6-zu-2-Kanal-Faltung die Teile des linken Ausgabe Kanals und den rechten Ausgabekanal dar, die aus dem linken Mitte-Kanal im 6-kanalstream bestehen.

Diese Eigenschaft sollte nur festgelegt werden, wenn vom Autor angegebene Fold-Werte mit dem codierten Inhalt persistent gespeichert werden. Andernfalls kann der Decoder seine eigenen Berechnungen durchführen lassen.

Der Windows Media Audio 10 Professional-Codec unterstützt zurzeit nur die Aufteilung auf zwei Kanäle.

Wenn die Eigenschaft [mfpkey \_ wmadec \_ spkrcfg](mfpkey-wmadec-spkrcfgproperty.md) auf **dsspeaker- \_ umschließen** festgelegt ist, ignoriert der Codec vom Autor bereitgestellte Fold-und-Zeichen, die vom Matrix Decoder des Empfängers verarbeitet werden können. Dadurch können umschließende Geräte vier Kanäle bereitstellt. Dieser Modus wird nur unterstützt, wenn die Quelle 5,1 ist. Der Codec kann nur acht Kanäle in zwei Kanäle Falten.

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

 

 
