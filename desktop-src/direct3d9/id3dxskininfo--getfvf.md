---
description: 'ID3DXSkinInfo::GetFVF-Methode: Ruft den festen Vertexwert der Funktion ab.'
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: ID3DXSkinInfo::GetFVF-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107158"
---
# <a name="id3dxskininfogetfvf-method"></a>ID3DXSkinInfo::GetFVF-Methode

Ruft den vertex-Wert der festen Funktion ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt die Codes des flexiblen Vertexformats (FVF) zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann 0 zurückgeben, wenn das Scheitelpunktformat nicht direkt einem FVF-Code zugeordnet werden kann. Dies tritt bei einem Gitternetz auf, das aus einer Scheitelpunktdeklaration erstellt wurde, die nicht die gleiche Reihenfolge und dieselben Elemente aufwies, die von den FVF-Codes unterstützt werden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetFVF**](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
