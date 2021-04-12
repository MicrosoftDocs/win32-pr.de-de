---
description: Ruft eine Technik Beschreibung ab.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'ID3DXBaseEffect:: gettechniquedesc-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219693"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a>ID3DXBaseEffect:: gettechniquedesc-Methode

Ruft eine Technik Beschreibung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htechnik* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Technik handle. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*PDE SC* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXTECHNIQUE \_ DESC**](d3dxtechnique-desc.md)\***

Gibt eine Beschreibung der Technik zurück. Weitere Informationen finden Sie unter [**D3DXTECHNIQUE \_**](d3dxtechnique-desc.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




