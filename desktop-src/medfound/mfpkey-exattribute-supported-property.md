---
description: Gibt an, ob Media Foundation -Transformation (MFT) Attribute aus Eingabebeispielen in Ausgabebeispiele kopiert.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED -Eigenschaft (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663509"
---
# <a name="mfpkey_exattribute_supported-property"></a>MFPKEY \_ EXATTRIBUTE \_ SUPPORTED (Eigenschaft)

Gibt an, ob Media Foundation -Transformation (MFT) Attribute aus Eingabebeispielen in Ausgabebeispiele kopiert.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Hinweise

Dieses Attribut kann die folgenden Werte haben.



| Wert              | Beschreibung                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | Der MFT kopiert Attribute aus den Eingabebeispielen in die Ausgabebeispiele.                                                                                 |
| **VARIANT \_ FALSE** | Die Mediensitzung kopiert Attribute aus Eingabebeispielen in Ausgabebeispiele. Es werden keine Attribute überschrieben, die der MFT für die Ausgabebeispiele festschreibt. |



 

Um dieses Attribut zu erhalten, rufen **Sie QueryInterface** für MFT für die **IPropertyStore-Schnittstelle** auf.

Der Standardwert ist **VARIANT \_ FALSE.** Wenn MFT die **IPropertyStore-Schnittstelle** nicht verfügbar macht oder diese Eigenschaft nicht festgelegt ist, behandeln Sie den Wert als **VARIANT \_ FALSE.**

Diese Eigenschaft ist schreibgeschützt.

> [!NOTE] 
> Dieses Attribut gilt nicht für asynchrone MFTs. Attribute werden unabhängig vom Wert dieses Attributs nicht aus den Eingabebeispielen in die Ausgabebeispiele für asynchrone MFTs kopiert.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird VARIANT \_ TRUE zurückgegeben, wenn ein MFT Beispielattribute kopiert.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Beispielattribute](sample-attributes.md)
</dt> <dt>

[**DURCHSICHTTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




