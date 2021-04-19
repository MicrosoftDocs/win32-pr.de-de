---
description: 'Berechnet einen Übertragungs Vektor, der die Quell Strahlung zum Beenden von Strahlen zuordnet, die sich aus der unter Surface-Aufteilung ergeben, wobei Adaptive Stichprobenentnahme und Materialeigenschaften verwendet werden, die von ID3DXPRTEngine:: setmeschmaterials'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine:: computess Adaptive-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365868"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>ID3DXPRTEngine:: computess Adaptive-Methode

Berechnet einen Übertragungs Vektor, der die Quell Strahlung zum Beenden von Strahlen zuordnet, die sich aus der unter Surface-Aufteilung ergeben, wobei Adaptive Stichprobenentnahme und Materialeigenschaften verwendet werden, die von [**ID3DXPRTEngine:: setmeschmaterials**](id3dxprtengine--setmeshmaterials.md) Die-Methode generiert neue Scheitel Punkte und Gesichter im Mesh, um das PRT-Signal (precompuradiance-Übertragung) genauer zu berechnen. Diese Methode kann nur für Materialien verwendet werden, die pro-Vertex in einem Mesh-Objekt definiert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdatain* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt. Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> <dt>

*Adaptivethresh* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Schwellenwert für den PRT-Vektor, der für die Unterteilung von Mesh-Scheitel Punkten und Flächen verwendet wird Wenn kleiner als 1E-6f ist, wird ein Standardwert von 1E-6f angegeben.

</dd> <dt>

*Minedgelength* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimale Vorderseiten Länge, die bei der adaptiven Stichproben Erstellung generiert wird. Wenn die Methode ermittelt, dass der Wert zu klein ist, wird ein Modell abhängiger Wert angegeben.

</dd> <dt>

*Maxsubdiv* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Maximale Ebene der Unterteilung einer Fläche, die bei der adaptiven Stichprobenentnahme verwendet wird. Wenn der Wert NULL ist, wird der Standardwert 4 angegeben.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Ein Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das einen einzelnen Sprung der unter Oberfläche durch verstreut-Licht modelliert. Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> <dt>

*pdatatotal* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, bei dem es sich um die laufende Summe aller vorherigen pdataout-Ausgaben handelt. Kann **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Um die unter Surface-Zerstreuung zu modellieren, wird diese Methode für jeden Licht Sprung aufgerufen, nachdem eine [**ID3DXPRTEngine:: computedirectlightingshadaptive**](id3dxprtengine--computedirectlightingshadaptive.md) -Methode aufgerufen wurde.

Die Ausgabe dieser Methode enthält nicht "Albedo", und nur das eingehende Licht ist in den Simulator integriert. Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.

[**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) aufzurufen, um jeden PRT-Vektor von Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computebounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine:: computess**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
