---
description: 'ID3DXBaseMesh::D rawSubset-Methode: Zeichnet eine Teilmenge eines Gitters.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: ID3DXBaseMesh::D rawSubset-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115468"
---
# <a name="id3dxbasemeshdrawsubset-method"></a>ID3DXBaseMesh::D rawSubset-Methode

Zeichnet eine Teilmenge eines Gitters.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AttribId* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD, das angibt, welche Teilmenge des Gitters ge zeichnen werden soll. Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als einer oder mehrere Attributgruppen zu unterscheiden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Die von AttribId angegebene Teilmenge wird von der [**IDirect3DDevice9::D rawIndexedPrimitive-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) mithilfe des primitiven D3DPT TRIANGLELIST-Typs gerendert, sodass ein Indexpuffer ordnungsgemäß initialisiert werden \_ muss.

Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (*AttribId*) gezeichnunget wird.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
