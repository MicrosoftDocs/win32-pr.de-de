---
title: 3D-Such Tabellen Effekt
description: Eine 3D-Nachschlage Tabelle ist ein allgemeiner Effekt, der verwendet wird, um jeden 1 1-Abbild Erstellungs Effekt zu kapseln, indem im Voraus berechnet wird, wie der Effekt Eingaben zu Ausgaben für eine Teilmenge aller Eingabewerte zuordnet.
ms.assetid: 2f0b4b6d-f371-101c-918a-bf564778e593
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0c6c5df1aa873d3458345d77a46f6f3fdae40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859320"
---
# <a name="3d-lookup-table-effect"></a>3D-Such Tabellen Effekt

Eine 3D-Nachschlage Tabelle ist ein allgemeiner Effekt, der verwendet wird, um jeden 1:1-Abbild Erstellungs Effekt zu kapseln, indem im Voraus berechnet wird, wie der Effekt Eingaben zu Ausgaben für eine Teilmenge aller Eingabewerte zuordnet.

Mit dem Text der 3D-Such Tabelle (LUT) wird ein Eingabebild geändert, indem der RGB-Farbwert des Bilds zum Indizieren einer 3D-Textur verwendet wird, wobei die Textur einen vorab berechneten Ausgabewert einer beliebigen Effekt Pipeline enthält.

Der 3D-LUT muss in eine GPU-Textur Ressource geladen werden, damit er gerendert werden kann. Dies kann in Abhängigkeit von der Größe der Textur und den Gerätefunktionen teuer sein. Anwendungsentwickler können angeben, wann diese Kosten mithilfe der [**ID2D1LookupTable3D**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d) D2D-Ressource abgerechnet werden sollen. **ID2D1LookupTable3D** hat die folgenden Attribute:

-   Stellt eine abstrahierte Darstellung der GPU-Ressource von 3D-LUT bereit.
-   Abhängig von den Gerätefunktionen wird entweder eine 2D-oder 3D-Textur erstellt und mit den bereitgestellten LUT-Daten gefüllt.
-   Kann zum Rendering an die-Eigenschaft des 3D-LUT-Effekts übermittelt werden.

Die CLSID für diesen Effekt ist CLSID \_ D2D1LookupTable3D.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für Effekte Ausgabe](images/3dlookuptable-effect.png)

## <a name="sample-code"></a>Beispielcode

```cpp
//
    // 1. Generate the lookup table data and create an ID2D1LookupTable3D.
    //
 
    // Create a 16x16x16 LUT of arbitrary data type T.
    UINT extents[] = { 16, 16, 16 };
    UINT cElements = extents[0] * extents[1] * extents[2] * 4;
    UINT cbElements = cElements * formatSize;
 
    // Compute the step size in each direction to vary the RGB 
    // channels uniformly over the range [0, 1]
    float steps[] = 
    { 
        1.0f / static_cast<float>(extents[0] - 1),
        1.0f / static_cast<float>(extents[1] - 1),
        1.0f / static_cast<float>(extents[2] - 1),
    };
 
    CArray<BYTE> lutData;
    IFR(lutData.Resize(cbElements));
 
    T* pData = reinterpret_cast<T *>(lutData.GetData());
    T oneValue = ConvertValue<T>(1.0f);
    
    // Generate the LUT by applying an imaging pipeline to RGB values.
    for (UINT iR = 0; iR < extents[2]; iR++)
    {
        for (UINT iG = 0; iG < extents[1]; iG++)
        {
            for (UINT iB = 0; iB < extents[0]; iB++)
            {
                T outputColor[3];
                ApplyPipeline(iR * steps[2], iG * steps[1], iB * steps[0], &outputColor);
 
                pData[0] = outColor[0];
                pData[1] = outColor[1];
                pData[2] = outColor[2];
 
                // Set opaque alpha in the output
                pData[3] = oneValue;
 
                // Advance the pointer
                pData += sizeof(T) * 4;
            }
        }
    }
    
    // Compute the strides of the LUT data.
    UINT strides[2];
    IFR(UIntMult(sizeof(T) * 4, extents[0], &strides[0]));
    IFR(UIntMult(strides[0], extents[1], &strides[1]));
    
    D2D1_BUFFER_PRECISION precision = GetBufferPrecision<T>();
 
    // Create an ID2D1LookupTable3D from the LUT data.
    CComPtr<ID2D1LookupTable3D> sp3dLut;
    IFR(_spEffectContext1->CreateLookupTable3D(
        precision,
        extents,
        lutData.GetData(),
        lutData.GetCount(),
        strides,
        &sp3dLut
        )); 
 
    //
    // 2. To apply the lookup table to an input image, create a LookupTable3D effect
    //    and pass the ID2D1LookupTable3D to the effect as a property.
    //
 
    // Create a 3D LUT effect to render our LUT.
    CComPtr<ID2D1Effect> sp3dLutEffect;
    IFR(pEffectContext->CreateEffect(CLSID_D2D1LookupTable3D, &sp3dLutEffect)); 
 
    // Set the LUT as a property on the effect.
    IFR(sp3dLutEffect->SetValue(D2D1_LOOKUPTABLE3D_PROP_LUT, _spLut));
```

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den 3D-Such Tabellen Effekt werden durch die [**D2D1 \_ LOOKUPTABLE3D \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_lookuptable3d_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
