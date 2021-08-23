---
description: Erstellen Sie einen Matrixstapel.
ms.assetid: df0f3564-0226-44b8-b22b-4dd27905c44c
title: D3DXCreateMatrixStack-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMatrixStack
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 90436f905c2470fd14b022a1c025737fa78726cf5e46286dec2e13d7392e9b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498350"
---
# <a name="d3dxcreatematrixstack-function-d3dx10mathh"></a>D3DXCreateMatrixStack-Funktion (D3DX10Math.h)

Erstellen Sie einen Matrixstapel.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  UINT              Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nicht implementiert. Geben Sie 0 (null) an.

</dd> <dt>

*ppStack* \[ out\]
</dt> <dd>

Typ: **LPD3DXMATRIXSTACK \***

Die Adresse eines Zeigers auf einen Matrixstapel (siehe [**ID3DXMatrixStack-Schnittstelle**](d3d10-id3dxmatrixstack.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
