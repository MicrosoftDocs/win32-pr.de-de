---
description: Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'ID3DX10SkinInfo:: addboneinfluences-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219530"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>ID3DX10SkinInfo:: addboneinfluences-Methode

Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Einfluss Zähler* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte, die dem knochenwert hinzugefügt werden sollen.

</dd> <dt>

*PIndizes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von Scheitelpunkt Indizes. Jedes Element dieses Arrays verfügt über einen entsprechenden Member in pgewichtungen, d. b., PIndizes \[ \] entsprechen den pgewichtungen \[ i \] . Der entsprechende Wert in pgewichtungen \[ i legt fest, \] wie viel Einfluss boneindex auf den Scheitelpunkt hat, der von PIndizes i indiziert wird \[ \] . Die Größe des PIndizes-Arrays muss größer oder gleich "Einfluss Wert" sein.

</dd> <dt>

*pgewichtungen* \[ in\]
</dt> <dd>

Typ: **float \***

Zeiger auf ein Array von Knochen Gewichtungen. Jedes Element dieses Arrays verfügt über einen entsprechenden Member in PIndizes, d. b., die pgewichtungen \[ \] entsprechen den PIndizes \[ i \] . Jeder Wert in pgewichtungen liegt zwischen 0 und 1 und definiert den Umfang der Auswirkung, den der Knochen über jedem Scheitelpunkt hat. Die Größe der pgewichtungen muss gleich oder größer als Einfluss Wert sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg oder e \_ oudef Memory.

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

 

 
