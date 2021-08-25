---
description: Gibt an, ob der Encoder beim Ausführen der VBR-Codierung mit zwei Durchläufen die Datenkonsistenz über Durchläufe hinweg überprüfen soll. Lese-/Schreibzugriff.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cef9c8c2a8e4fcd536ce73653e80e62282b40734cc695493d6cba4187c8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954720"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>MFPKEY \_ CHECKDATACONSISTENCY2P-Eigenschaft

Gibt an, ob der Encoder beim Ausführen der VBR-Codierung mit zwei Durchläufen die Datenkonsistenz über Durchläufe hinweg überprüfen soll. Lese-/Schreibzugriff.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ TRUE**

## <a name="remarks"></a>Hinweise

Wenn Sie diese Eigenschaft bei ihrem Standardwert **VARIANT \_ TRUE** belassen, überprüft der Encoder, ob die Eingabebeispiele zwischen den beiden Durchläufen übereinstimmen, und schlägt fehl, wenn eine Abweichung erkannt wird. Das Hauptszenario, das zu einer Diskrepanz führt, ist, wenn die Eingabe von einem Gerät stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
