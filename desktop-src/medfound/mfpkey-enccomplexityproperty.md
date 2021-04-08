---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: 5dd34818-f282-4859-b423-97e9c4944aec
title: MFPKEY_ENCCOMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51f50e7966a05affe8ae75869b670cf75f088b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864164"
---
# <a name="mfpkey_enccomplexity-property"></a>Mfpkey \_ enckomplexität (Eigenschaft)

Gibt die Komplexität des Codierungs Algorithmus an. Der Wert ist eine ganze Zahl zwischen 0 und 100, wobei 0 den am wenigsten komplexen Algorithmus und 100 den komplexesten Algorithmus angibt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

100 für Windows Media Audio 10 und Windows Media Audio 10 Professional

100 für die Windows Vista-Version von Windows Media Audio 10 verlustfrei

0 für Windows 7 Release Windows Media Audio 10 verlustfreie Version

## <a name="remarks"></a>Bemerkungen

Wenn die Eigenschaft [**mfpkey \_ einschränationskomplexität**](mfpkey-constrainenccomplexityproperty.md) den Wert **Variant \_ true** hat, passt der Encoder die Komplexität seines Algorithmus entsprechend dem Wert dieser Eigenschaft an.

Für den Windows Media Audio 10-Encoder und den Windows Media Audio 10 Professional-Encoder, wenn der Wert dieser Eigenschaft 100 ist, stellt der Encoder einen hohen Bedarf an der CPU her und erzeugt die höchst wertige Ausgabe. Wenn der Wert dieser Eigenschaft abnimmt, sinkt die Nachfrage nach der CPU, aber die Qualität der Ausgabe wird ebenfalls verringert.

Wenn der Wert dieser Eigenschaft auf 0 (null) gesetzt ist und der Wert dieser Eigenschaft auf 0 (null) gesetzt ist, stellt der Encoder für den Windows Media Audio 10-Encoder ohne Verlust Wenn der Wert dieser Eigenschaft zunimmt, steigt der Bedarf an der CPU, und die Größe der Encoder-Ausgabe nimmt geringfügig ab. Die Ausgabe ist unabhängig vom Wert dieser Eigenschaft verlustfrei.

Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, verwendet der Encoder seinen Standard Algorithmus. Der Standard Algorithmus hängt davon ab, welchen Encoder Sie verwenden und welche Version von Windows ausgeführt wird. In der folgenden Tabelle wird das Standardverhalten für die verschiedenen Kombinationen beschrieben.



| Betriebssystem | Standardverhalten                                                                                                                                                                                                |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Die Windows Media Audio 10, Windows Media Audio 10 Professional und die Windows Media Audio 10 Verlust lose Encoder verwenden standardmäßig den komplexesten Algorithmus.                                                    |
| Windows 7        | Die Windows Media Audio 10-und Windows Media Audio 10 Professional Encoder verwenden standardmäßig den komplexesten Algorithmus. Der Windows Media Audio 10-Encoder ohne Verlust verwendet standardmäßig den am wenigsten komplexen Algorithmus. |



 

Wenn die Eigenschaft [**mfpkey \_ einschränationskomplexität**](mfpkey-constrainenccomplexityproperty.md) den Wert **Variant \_ false** aufweist, ignoriert der Encoder diese Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
