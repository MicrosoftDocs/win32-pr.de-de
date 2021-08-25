---
description: 'D3DXCheckVersion-Funktion: Stellen Sie sicher, dass die D3DX-Version, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.'
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
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894120"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion-Funktion

Stellen Sie sicher, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.

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

Verwenden Sie die D3DX \_ \_ SDK-VERSION. Siehe Bemerkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE zurück,** wenn die Version von D3DX, für die Sie kompiliert haben, die Version ist, mit der Sie ausführen. Andernfalls **wird FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion während der Initialisierung Ihrer Anwendung wie die folgenden:


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



Verwenden [**Sie Direct3DCreate9,**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) um zu überprüfen, ob die richtige Runtime installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
