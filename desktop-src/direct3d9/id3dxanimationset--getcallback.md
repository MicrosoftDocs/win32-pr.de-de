---
description: Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet:: getCallback-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219699"
---
# <a name="id3dxanimationsetgetcallback-method"></a>ID3DXAnimationSet:: getCallback-Methode

Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.

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

*Position* \[ in\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)**

Die Position, an der Rückrufe gesucht werden sollen.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Rückruf Suchflags. Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus [**D3DXCALLBACK- \_ \_ Suchflags**](./d3dxcallback-search-flags.md)festgelegt werden.

</dd> <dt>

*pcallbackposition* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **Double**](../winprog/windows-data-types.md)\***

Ein Zeiger auf die Position des Rückrufs.

</dd> <dt>

*ppcallbackdata* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Adresse des Rückruf Daten Zeigers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
