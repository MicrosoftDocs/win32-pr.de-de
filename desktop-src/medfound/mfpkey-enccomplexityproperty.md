---
description: Gibt die Komplexität des Codierungsalgorithmus an.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93abe02b50f862fec706f75449e00643228a3917bc22ca9dafa9285d9d46be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117690125"
---
# <a name="mfpkey_enccomplexity-property"></a>MFPKEY \_ ENCCOMPLEXITY-Eigenschaft

Gibt die Komplexität des Codierungsalgorithmus an. Der Wert ist eine ganze Zahl zwischen 0 und 100, wobei 0 den am wenigsten komplexen Algorithmus und 100 den komplexesten Algorithmus angibt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

100 für Windows Media Audio 10 und Windows Media Audio 10 Professional

100 für die Windows Vista-Version von Windows Media Audio 10 Lossless

0 für Windows 7 release Windows Media Audio 10 Lossless

## <a name="remarks"></a>Hinweise

Wenn die [**MFPKEY \_ CONSTRAINECOMPLEXITY-Eigenschaft**](mfpkey-constrainenccomplexityproperty.md) über den Wert **VARIANT \_ TRUE** verfügt, passt der Encoder die Komplexität seines Algorithmus entsprechend dem Wert dieser Eigenschaft an.

Wenn der Windows Media Audio 10-Encoder und der Windows Media Audio 10-Professional Encoder den Wert 100 haben, stellt der Encoder einen hohen Bedarf an der CPU und erzeugt die ausgabestärkste Ausgabe. Wenn der Wert dieser Eigenschaft abnimmt, sinkt die CPU-Nachfrage, aber auch die Qualität der Ausgabe nimmt ab.

Wenn der Wert dieser Eigenschaft für den Windows Media Audio 10 Lossless-Encoder 0 ist, stellt der Encoder einen geringen Bedarf an der CPU. Wenn der Wert dieser Eigenschaft zunimmt, steigt der Bedarf an der CPU, und die Größe der Encoderausgabe nimmt leicht ab. Die Ausgabe ist unabhängig vom Wert dieser Eigenschaft verlustfrei.

Wenn Sie diese Eigenschaft beim Standardwert **VARIANT \_ FALSE** belassen, verwendet der Encoder seinen Standardalgorithmus. Der Standardalgorithmus hängt davon ab, welchen Encoder Sie verwenden und welche Version von Windows ausgeführt wird. In der folgenden Tabelle wird das Standardverhalten für die verschiedenen Kombinationen beschrieben.



| Betriebssystem | Standardverhalten                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Die Windows Media Audio 10, Windows Media Audio 10 Professional und Windows Media Audio 10 Lossless Encoder verwenden standardmäßig den komplexesten Algorithmus.                                                    |
| Windows 7        | Die Windows Media Audio 10 und Windows Media Audio 10 Professional Encoder verwenden standardmäßig den komplexesten Algorithmus. Der Windows Media Audio 10 Lossless Encoder verwendet standardmäßig den am wenigsten komplexen Algorithmus. |



 

Wenn die [**MFPKEY \_ CONSTRAINECOMPLEXITY-Eigenschaft**](mfpkey-constrainenccomplexityproperty.md) über den Wert **VARIANT \_ FALSE** verfügt, ignoriert der Encoder diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
