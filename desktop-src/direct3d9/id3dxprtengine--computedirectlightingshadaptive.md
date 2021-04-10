---
description: Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung mithilfe der adaptiven Stichprobenentnahme durch eine Glanz Näherung (SH) dargestellt wird.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine:: computedirectlightingshadaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762375"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>ID3DXPRTEngine:: computedirectlightingshadaptive-Methode

Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung mithilfe der adaptiven Stichprobenentnahme durch eine Glanz Näherung (SH) dargestellt wird. Diese Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*Adaptivethresh* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Schwellenwert für den PRT-Vektor, der für die Unterteilung von Mesh-Scheitel Punkten und Flächen verwendet wird Wenn kleiner als 1E-6f ist, wird ein Standardwert von 1E-6f angegeben.

</dd> <dt>

*Minedgelength* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird. Wenn die Methode ermittelt, dass der Wert zu klein ist, wird ein Modell abhängiger Wert angegeben. Wenn der Wert NULL ist, wird der Standardwert 4 angegeben.

</dd> <dt>

*Maxsubdiv* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt. Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
