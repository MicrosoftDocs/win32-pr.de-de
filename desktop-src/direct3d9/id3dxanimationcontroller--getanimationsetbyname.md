---
description: Ruft einen Animations Satz mit dem angegebenen Namen ab.
ms.assetid: 4c3f3002-45f6-49b2-8a42-18d5824fb36f
title: 'ID3DXAnimationController:: getanimationsetbyname-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: d520625e457a50fe962ae74d6e25fc17e2beb729
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354396"
---
# <a name="id3dxanimationcontrollergetanimationsetbyname-method"></a>ID3DXAnimationController:: getanimationsetbyname-Methode

Ruft einen Animations Satz mit dem angegebenen Namen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnimationSetByName(
  [in]  LPCSTR             pName,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeichenfolge, die den Namen des Animations Satzes enthält.

</dd> <dt>

*ppanimset* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Der Animations Controller enthält ein Array von Animations Sätzen. Diese Methode gibt einen Animations Satz mit dem angegebenen Namen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
