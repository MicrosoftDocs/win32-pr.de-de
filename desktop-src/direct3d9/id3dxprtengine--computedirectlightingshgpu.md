---
description: Verwendet die GPU, um den direkten Beleuchtungs Beitrag zu 3D-Objekten zu berechnen, wobei die Quell Ausstrahlung durch eine Glanz förmige Näherung (SH) dargestellt wird. Das Berechnen der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine:: computedirectlightingshgpu-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365352"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>ID3DXPRTEngine:: computedirectlightingshgpu-Methode

Verwendet die GPU, um den direkten Beleuchtungs Beitrag zu 3D-Objekten zu berechnen, wobei die Quell Ausstrahlung durch eine Glanz förmige Näherung (SH) dargestellt wird. Das Berechnen der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Geräte Objekt, das verwendet wird, um die Simulation auf der GPU auszuführen. Das Gerät muss [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) Pixel Shader unterstützen.

> [!Note]  
> Rückruf Funktionen dürfen nicht das [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Geräte Objekt verwenden, das vom GPU-Simulator verwendet wird.

 

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der GPU-Simulations Parameter, der die Auflösung des Schatten-z-Puffers definiert. Muss auf einen der Konstanten Werte aus [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md)festgelegt werden. Der D3DXSHGPUSIMOPT \_ HighQuality-Wert kann mit einem der D3DXSHGPUSIMOPT shadowresxxx-Werte kombiniert werden, um die Simulation mit einer höheren Genauigkeit zu spezifiken \_ .

</dd> <dt>

*Reihenfolge* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der SH-Evaluierung. Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen. Die Auswertung generiert die Koeffizienten der Bestellung. Der Bewertungs Grad ist Order-1.

</dd> <dt>

*Zbias* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

In normaler Richtung ausrichten.

</dd> <dt>

*Zanglebias* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Wird in normaler Richtung gemessen und um eins abzüglich des Kosinus des Winkels mit dem Lichtstrahl skaliert.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt. Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Bei dieser Methode wird die Albedo-Methode nicht mit dem Lichtsignal multipliziert, und nur das eingehende Licht ist in den Simulator integriert. Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.

Rufen Sie [**multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) auf, um die einzelnen PRT-Vektoren (preberechneten Radiance Transfer) von Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
