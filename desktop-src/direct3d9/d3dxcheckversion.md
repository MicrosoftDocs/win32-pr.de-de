---
description: 'D3DXCheckVersion-Funktion: Vergewissern Sie sich, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: D3DXCheckVersion-Funktion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 077d64a67a46080a0f7ac9194c684f6fe8470453
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115978"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion-Funktion

Vergewissern Sie sich, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*D3DSDKVersion* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Verwenden Sie die D3D \_ \_ SDK-VERSION. Siehe Bemerkungen.

</dd> <dt>

*D3DXSDKVersion* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Verwenden Sie die Version des D3DX \_ \_ SDK. Siehe Bemerkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn die Version von D3DX, für die Sie kompiliert haben, die Version ist, mit der Sie ausgeführt werden. andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion während der Initialisierung Ihrer Anwendung wie folgt:


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Verwenden Sie [**Direct3DCreate9,**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) um zu überprüfen, ob die richtige Runtime installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
