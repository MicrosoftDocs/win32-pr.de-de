---
description: Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quellstrahlstärke durch eine Sphärische Gleichung (SH)-Näherung dargestellt wird.
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: ID3DXPRTEngine::ComputeDirectLightingSH-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51eb3121501cee7c56385a9083fc689cd8a06759443250f64bae16901779a3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729712"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>ID3DXPRTEngine::ComputeDirectLightingSH-Methode

Berechnet den direkten Beleuchtungsbeitrag zu 3D-Objekten, bei denen die Quellstrahlstärke durch eine Sphärische Gleichung (SH)-Näherung dargestellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bestellung* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reihenfolge der SH-Auswertung. Muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen. Die Auswertung generiert Order²-Koeffizienten. Der Grad der Auswertung ist "Order - 1".

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein [**ID3DXPRTBuffer-Ausgabeobjekt,**](id3dxprtbuffer.md) das den direkten Beleuchtungsbeitrag mit der SH-Näherung modelliert. Diesem Puffer muss die richtige Anzahl von Farbkanälen für die Simulation zugeordnet sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Die Ausgabe enthält kein Albedo, und nur eingehendes Licht ist in den Simulator integriert. Indem Sie den Albedo nicht multiplizieren, können Sie die Albedo-Variation in einer feineren Skala als die Quellleistung modellieren und so genauere Ergebnisse der Komprimierung erzielen.

Rufen Sie [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) auf, um jeden voraus berechneten PRT-Vektor (Radiance Transfer) mit dem Albedo zu multiplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
