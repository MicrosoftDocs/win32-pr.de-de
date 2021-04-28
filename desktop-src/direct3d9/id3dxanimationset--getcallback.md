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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097538"
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

Position, an der Rückrufe zu finden sind.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Rückrufsuchflags. Dieser Parameter kann auf eine Kombination aus mindestens einem Flag aus [**D3DXCALLBACK-SUCHFLAgs \_ \_ festgelegt werden.**](./d3dxcallback-search-flags.md)

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

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR zurückgegeben wird.**](./d3dxerr.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
