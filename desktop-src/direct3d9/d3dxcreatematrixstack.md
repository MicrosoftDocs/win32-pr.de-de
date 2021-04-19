---
description: Erstellt eine Instanz der ID3DXMATRIXStack-Schnittstelle.
ms.assetid: bb067b38-efc6-4ed8-9eef-14b3cc70660f
title: D3DXCreateMatrixStack-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 08e1ac23d5f6bcd874b1d5bd7f60313a232b0563
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373537"
---
# <a name="d3dxcreatematrixstack-function-d3dx9mathh"></a>D3DXCreateMatrixStack-Funktion (D3dx9math. h)

Erstellt eine Instanz der [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateMatrixStack(
  _In_  DWORD             Flags,
  _Out_ LPD3DXMATRIXSTACK *ppStack
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nicht implementiert. Geben Sie NULL an.

</dd> <dt>

*ppstack* \[ vorgenommen\]
</dt> <dd>

Typ: **LPD3DXMATRIXSTACK \***

Adresse eines Zeigers, der mit einem [**ID3DXMATRIXStack**](id3dxmatrixstack.md) -Schnittstellen Zeiger gefüllt wird, wenn die Funktion erfolgreich ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
