---
description: Gibt die Treiber Ebene zurück.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: D3DXGetDriverLevel-Funktion (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355187"
---
# <a name="d3dxgetdriverlevel-function"></a>D3DXGetDriverLevel-Funktion

Gibt die Treiber Ebene zurück.

## <a name="syntax"></a>Syntax


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Treiber Ebene. Siehe Bemerkungen.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt die Treiber Version zurück, die eines der folgenden ist:

-   700-Direct3D 7-Ebenen-Treiber
-   800-Direct3D 8-Ebenen-Treiber
-   900-Direct3D 9-sestreiber

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
