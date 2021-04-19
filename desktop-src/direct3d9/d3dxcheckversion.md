---
description: Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: D3DXCheckVersion-Funktion (D3dx9core. h)
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366660"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion-Funktion

Vergewissern Sie sich, dass die Version von D3DX, die Sie mit kompiliert haben, die Version ist, die Sie ausführen.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*D3DSDKVersion* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Verwenden Sie die D3D \_ SDK- \_ Version. Siehe Bemerkungen.

</dd> <dt>

*D3DXSDKVersion* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Verwenden Sie die D3DX \_ SDK- \_ Version. Siehe Bemerkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt **true** zurück, wenn die Version von D3DX, die Sie für kompiliert haben, die Version ist, mit der Sie ausführen. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion während der Initialisierung der Anwendung wie folgt:


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



Verwenden Sie [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) , um zu überprüfen, ob die richtige Laufzeit installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
