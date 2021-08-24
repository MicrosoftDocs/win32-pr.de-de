---
title: D3DX11_ERR -Enumeration (D3DX11.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR-Enumeration Direct3D 11
- LPD3DX11_ERR-Enumerationszeiger Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80b906b5b95693458eeea353f40fe446a22e8e33a6011b7851cf6d9663b3ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729320"
---
# <a name="d3dx11_err-enumeration"></a>D3DX11 \_ ERR-Enumeration

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden. Im Folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX-Hilfsprogrammbibliothek enthalten sind. Listen der Werte, die jeweils zurückgeben können, finden Sie in den Beschreibungen der einzelnen Methoden. Diese Listen sind nicht unbedingt umfassend.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ ERR \_ KANN \_ INDEXPUFFER NICHT \_ \_ ÄNDERN**
</dt> <dd>

Der Indexpuffer kann nicht geändert werden.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ ERR \_ INVALID \_ MESH**
</dt> <dd>

Das Gitternetz ist ungültig.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ ERR \_ CANNOT \_ ATTR \_ SORT**
</dt> <dd>

Die Attributsortierung (D3DXMESHOPT \_ ATTRSORT) wird als Optimierungsmethode nicht unterstützt.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ ERR \_ SKINNING \_ NICHT \_ UNTERSTÜTZT**
</dt> <dd>

Skinning wird nicht unterstützt.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ ERR \_ TOO \_ MANY \_ INFLUENCES**
</dt> <dd>

Es wurden zu viele Faktoren angegeben.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ ERR \_ UNGÜLTIGE \_ DATEN**
</dt> <dd>

Die Daten sind ungültig.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 \_ ERR \_ LOADED \_ MESH \_ HAS \_ NO \_ DATA**
</dt> <dd>

Das Gitternetz verfügt über keine Daten.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ ERR \_ DUPLICATE \_ NAMED \_ FRAGMENT**
</dt> <dd>

Ein Fragment mit diesem Namen ist bereits vorhanden.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ ERR \_ KANN LETZTES ELEMENT \_ NICHT \_ \_ ENTFERNEN**
</dt> <dd>

Das letzte Element kann nicht gelöscht werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Einrichtungscode \_ FACDD wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros zu sehen.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX11.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





