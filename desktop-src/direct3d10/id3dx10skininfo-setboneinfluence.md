---
description: Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'ID3DX10SkinInfo:: setboneingefluence-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355215"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a>ID3DX10SkinInfo:: setboneingefluence-Methode

Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Einflussfaktor ceindex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index in der Liste der in der Liste der von ihm Einfluss enden Scheitel Punkte.

</dd> <dt>

*Gewichtung* \[ in\]
</dt> <dd>

Typ: **float**

Die Menge der Auswirkung zwischen 0 und 1, die der Knochen über dem Scheitelpunkt hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ invalidArg lauten.

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

 

 
