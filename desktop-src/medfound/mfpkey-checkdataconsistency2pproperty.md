---
description: Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll. Lese-/Schreibzugriff.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371983"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>Mfpkey \_ CHECKDATACONSISTENCY2P-Eigenschaft

Gibt an, ob der Encoder bei der Durchführung einer zweistufigen VBR-Codierung eine übergreifende Datenkonsistenz überprüfen soll. Lese-/Schreibzugriff.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ true**

## <a name="remarks"></a>Bemerkungen

Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ true** belassen, überprüft der Encoder, ob die Eingabe Beispiele zwischen den beiden Durchläufen Stimmen, und schlägt fehl, wenn eine Abweichung erkannt wird. Das wichtigste Szenario, das zu einer Abweichung führt, besteht darin, dass die Eingabe von einem Gerät stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
