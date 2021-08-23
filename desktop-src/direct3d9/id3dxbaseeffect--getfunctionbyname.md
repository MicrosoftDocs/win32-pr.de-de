---
description: Ruft das Handle einer Funktion ab, indem ihr Name gesucht wird.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: ID3DXBaseEffect::GetFunctionByName-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bcc16fa8136332e2a5d1a87956e1d4cc6a2a562b7e4e3531efbcc09f1314978b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121973"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a>ID3DXBaseEffect::GetFunctionByName-Methode

Ruft das Handle einer Funktion ab, indem ihr Name gesucht wird.

## <a name="syntax"></a>Syntax


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Eine Zeichenfolge, die den Funktionsnamen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Gibt das Handle der angegebenen Funktion oder **NULL zurück,** wenn der Name nicht gefunden wurde. Siehe [Handles (Direct3D 9).](handles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
