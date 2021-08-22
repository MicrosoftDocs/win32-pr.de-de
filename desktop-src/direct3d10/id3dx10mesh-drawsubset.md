---
description: 'ID3DX10Mesh::D rawSubset-Methode: Zeichnet eine Teilmenge eines Gitternetzes.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: ID3DX10Mesh::D rawSubset-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 75723819ab7a4f82f25a68dfc2f0017e8b871130a8e0fbe70c939a95de221426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753100"
---
# <a name="id3dx10meshdrawsubset-method"></a>ID3DX10Mesh::D rawSubset-Methode

Zeichnet eine Teilmenge eines Gitternetzes.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AttribId* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Gibt an, welche Teilmenge des Gitternetzes gezeichnet werden soll. Dieser Wert wird verwendet, um Gesichter in einem Gitternetz als zu einer oder mehreren Attributgruppen gehörend zu unterscheiden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen. Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitternetzes auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner (AttribId) gezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
