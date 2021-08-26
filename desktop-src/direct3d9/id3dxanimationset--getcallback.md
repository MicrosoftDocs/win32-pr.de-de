---
description: 'ID3DXAnimationSet::GetCallback-Methode: Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: ID3DXAnimationSet::GetCallback-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ded66bbe90320250667511d1c9468073693ce789cdb7add8574f42a4756136d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026590"
---
# <a name="id3dxanimationsetgetcallback-method"></a>ID3DXAnimationSet::GetCallback-Methode

Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Position* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Position, von der rückrufe gesucht werden sollen.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Rückrufsuchflags. Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus [**D3DXCALLBACK \_ SEARCH \_ FLAGS**](./d3dxcallback-search-flags.md)festgelegt werden.

</dd> <dt>

*pCallbackPosition* \[ out\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)\***

Zeiger auf die Position des Rückrufs.

</dd> <dt>

*ppCallbackData* \[ out\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Adresse des Rückrufdatenzeigers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode, um D3D \_ OK zurückzugeben. Programmieren Sie andernfalls die -Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
