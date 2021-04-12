---
description: Ruft die Anzahl der Einflüsse für einen Knochen ab.
ms.assetid: 6383f990-2989-46b3-a634-b3bb7bd1d65b
title: 'ID3DXSkinInfo:: getnumboneingefluences-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetNumBoneInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 712f54b0459bc3e62c61b59d001a5d27dd5a8837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219429"
---
# <a name="id3dxskininfogetnumboneinfluences-method"></a>ID3DXSkinInfo:: getnumboneingefluences-Methode

Ruft die Anzahl der Einflüsse für einen Knochen ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNumBoneInfluences(
  [in] DWORD bone
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Knochen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die Knochen Nummer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Anzahl der Einflüsse für einen Knochen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
