---
description: Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'ID3DX10SkinInfo:: getboneinfludencecount-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366468"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a>ID3DX10SkinInfo:: getboneinfluscecount-Methode

Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.

## <a name="syntax"></a>Syntax


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
