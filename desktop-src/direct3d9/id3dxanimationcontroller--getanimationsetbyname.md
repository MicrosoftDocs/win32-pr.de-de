---
description: Ruft einen Animationssatz mit seinem Namen ab.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: ID3DXAnimationController::GetAnimationSetByName-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSetByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b417bf9434b712903e61839807f71765b2e3c69916430f162a67febe65fc6cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297043"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a>ID3DXAnimationController::GetAnimationSetByName-Methode

Ruft einen Animationssatz mit seinem Namen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Namen des Animationssatzes enthält.

</dd> <dt>

*ppAnimSet* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Zeiger auf den [**ID3DXAnimationSet-Animationssatz.**](id3dxanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Der Animationscontroller enthält ein Array von Animationssätzen. Diese Methode gibt einen Animationssatz mit dem angegebenen Namen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
