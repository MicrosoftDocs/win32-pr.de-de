---
description: Gibt an, ob eine Media Foundation Transformation (MFT) Attribute aus Eingabe Beispielen in Ausgabe Beispiele kopiert.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED-Eigenschaft (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864160"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_Unterstützte Eigenschaft "mfpkey exattribute" \_

Gibt an, ob eine Media Foundation Transformation (MFT) Attribute aus Eingabe Beispielen in Ausgabe Beispiele kopiert.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**Variant \_ bool**

VT \_ bool

**Boolesche Werte**



## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann die folgenden Werte aufweisen.



| Wert              | BESCHREIBUNG                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Variant \_ true**  | Die MFT kopiert Attribute aus den Eingabe Beispielen in die Ausgabe Beispiele.                                                                                 |
| **Variant \_ false** | Die Medien Sitzung kopiert Attribute aus Eingabe Beispielen in Ausgabe Beispiele. Er überschreibt keine Attribute, die der MFT für die Ausgabe Beispiele festlegt. |



 

Zum Abrufen dieses Attributs aufrufen Sie **QueryInterface** für die **IPropertyStore** -Schnittstelle.

Der Standardwert ist **Variant \_ false**. Wenn die MFT die **IPropertyStore** -Schnittstelle nicht verfügbar macht oder diese Eigenschaft nicht festgelegt ist, wird der Wert als **Variant \_ false** behandelt.

Diese Eigenschaft ist schreibgeschützt.

> [!NOTE] 
> Dieses Attribut gilt nicht für asynchrone MFTs. Attribute werden nicht unabhängig vom Wert dieses Attributs aus den Eingabe Beispielen in die Ausgabe Beispiele für asynchrone MFTs kopiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird Variant true zurückgegeben, \_ Wenn ein MFT Beispiel Attribute kopiert.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Beispiel Attribute](sample-attributes.md)
</dt> <dt>

[**IMF Transform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




