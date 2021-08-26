---
description: Verwendet die GPU, um den direkten Beleuchtungsbeitrag zu 3D-Objekten zu berechnen, bei denen die Quelllichtleistung durch eine pherische Schwingung (SH) dargestellt wird. Die Berechnung der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: ID3DXPRTEngine::ComputeDirectLightingSLKPU-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 14dc76cb8ac3875101c42beb581c7eb2b96eb7511c85e7f76cd034658afcca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985580"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>ID3DXPRTEngine::ComputeDirectLightingSLKPU-Methode

Verwendet die GPU, um den direkten Beleuchtungsbeitrag zu 3D-Objekten zu berechnen, bei denen die Quelllichtleistung durch eine pherische Schwingung (SH) dargestellt wird. Die Berechnung der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.

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

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf das [**IDirect3DDevice9-Geräteobjekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das zum Ausführen der Simulation auf der GPU verwendet wird. Das Gerät muss Shader [mit \_ ps 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) Pixel unterstützen.

> [!Note]  
> Rückruffunktionen sollten nicht das [**IDirect3DDevice9-Geräteobjekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) verwenden, das vom GPU-Simulator verwendet wird.

 

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

GPU-Simulationsparameter, der die Auflösung des Schatten-Z-Puffers definiert. Sollte auf einen der konstanten Werte aus [**D3DXSLKPUSLIPPT festgelegt werden.**](./d3dxshgpusimopt.md) Zur Spezifikation einer Simulation mit höherer Genauigkeit kann der D3DXSLKPUSKATPT HIGHQUALITY-Wert mit einem der \_ D3DXSLKPUSLIPPT \_ SHADOWRESxxx-Werte kombiniert werden.

</dd> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order Koeffizienten. Der Grad der Auswertung ist Order - 1.

</dd> <dt>

*ZBias* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Voreingenommenheit in normaler Richtung.

</dd> <dt>

*ZAngleBias* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Voreingenommenheit in normaler Richtung, skaliert um eins minus dem Kosinus des Winkels mit dem Lichtstrahl.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Objekt.**](id3dxprtbuffer.md) Für diesen Puffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Bei dieser Methode wird der Albedo nicht mit dem Lichtsignal multipliziert, und nur eingehendes Licht ist in den Simulator integriert. Wenn Sie die Albedo nicht multiplizieren, können Sie Albedo-Variationen mit einer feineren Skala als die Quellbreite modellieren, wodurch genauere Ergebnisse der Komprimierung erzielt werden.

Rufen [**Sie MultiplyAlbedo auf,**](id3dxprtengine--multiplyalbedo.md) um jeden vorberechnungeten PRT-Vektor (Radiance Transfer) mit dem Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
