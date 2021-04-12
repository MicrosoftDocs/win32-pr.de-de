---
description: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: D3DXERR-Enumeration (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219517"
---
# <a name="d3dxerr-enumeration"></a>D3DXERR-Enumeration

Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden. Im folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX Utility Library enthalten sind. In den einzelnen Methodenbeschreibungen finden Sie Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können. Diese Listen sind nicht notwendigerweise vollständig.

## <a name="syntax"></a>Syntax


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ cannotmodifyindexbuffer**
</dt> <dd>

Der Index Puffer kann nicht geändert werden.

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ invalidmesh**
</dt> <dd>

Das Mesh ist ungültig.

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ cannotattrsort**
</dt> <dd>

Die Attribut Sortierung (D3DXMESHOPT \_ attrsort) wird nicht als Optimierungstechnik unterstützt.

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ skinningnotsupported**
</dt> <dd>

Das Skinning wird nicht unterstützt.

</dd> <dt>

<span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR- \_ Informationen**
</dt> <dd>

Es wurden zu viele Einflüsse angegeben.

</dd> <dt>

<span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ InvalidData**
</dt> <dd>

Die Daten sind ungültig.

</dd> <dt>

<span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ loadedmeshasnodata**
</dt> <dd>

Das Mesh weist keine Daten auf.

</dd> <dt>

<span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ duplialisienamedfragment**
</dt> <dd>

Ein Fragment mit diesem Namen ist bereits vorhanden.

</dd> <dt>

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ cannotremuvelastitem**
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
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




