---
description: Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: ID3DXBaseEffect::SetValue-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2bb619c9d0ef469b36f96d1e35ee70719ede8f6eee494cc950f6fabadbf86304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748970"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>ID3DXBaseEffect::SetValue-Methode

Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der Daten enthält.

</dd> <dt>

*Bytes* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

\[in \] Anzahl von Bytes im Puffer. Übergeben Sie D3DX DEFAULT, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie \_ die Größenüberprüfung überspringen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode kann statt fast aller API-Aufrufe des Effektensets verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
