---
description: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR-Enumeration (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 098c15999f20a65614d642029b1d1f6e0b600db6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219468"
---
# <a name="d3dx10_err-enumeration"></a>D3dx10 \_ Err-Enumeration

Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden. Im folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX Utility Library enthalten sind. In den einzelnen Methodenbeschreibungen finden Sie Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können. Diese Listen sind nicht notwendigerweise vollständig.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3dx10 \_ Err \_ kann \_ den \_ Index \_ Puffer nicht ändern**
</dt> <dd>

Der Index Puffer kann nicht geändert werden.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3dx10 \_ Err ( \_ ungültiges \_ Mesh)**
</dt> <dd>

Das Mesh ist ungültig.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3dx10 \_ Err \_ kann nicht in der \_ \_ Sortierreihenfolge**
</dt> <dd>

Die Attribut Sortierung (D3DXMESHOPT \_ attrsort) wird nicht als Optimierungstechnik unterstützt.

</dd> <dt>

<span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3dx10 \_ Err- \_ Skinning \_ \_ wird nicht unterstützt.**
</dt> <dd>

Das Skinning wird nicht unterstützt.

</dd> <dt>

<span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3dx10 \_ Err \_ zu \_ viele \_ Einflüsse**
</dt> <dd>

Es wurden zu viele Einflüsse angegeben.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3dx10 \_ Err \_ ungültige \_ Daten**
</dt> <dd>

Die Daten sind ungültig.

</dd> <dt>

<span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3dx10 \_ Err \_ geladenes \_ Mesh \_ hat \_ keine \_ Daten**
</dt> <dd>

Das Mesh weist keine Daten auf.

</dd> <dt>

<span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3dx10 \_ Err- \_ doppeltes \_ benanntes \_ Fragment**
</dt> <dd>

Ein Fragment mit diesem Namen ist bereits vorhanden.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3dx10 \_ Err \_ kann \_ das \_ Letzte \_ Element nicht entfernen.**
</dt> <dd>

Das letzte Element kann nicht gelöscht werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Einrichtungs Code- \_ fakdd wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros.


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
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




