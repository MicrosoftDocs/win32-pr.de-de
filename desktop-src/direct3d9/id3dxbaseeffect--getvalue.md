---
description: Hier erhalten Sie den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen. Diese Methode kann statt fast aller Getxxx-Aufrufe in ID3DXBaseEffect verwendet werden.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: ID3DXBaseEffect::GetValue-Methode (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f957ae3b59f10a086f2326e82478afb6b0ba7fd85bbf6b3f78df5746b7fcb56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494700"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>ID3DXBaseEffect::GetValue-Methode

Hier erhalten Sie den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichenfolgen, Shader und Texturen. Diese Methode kann statt fast aller Getxxx-Aufrufe in [**ID3DXBaseEffect verwendet werden.**](id3dxbaseeffect.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hParameter* \[ In\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Siehe [Handles (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Gibt einen Puffer zurück, der den Wert enthält.

</dd> <dt>

*Bytes* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

\[in \] Anzahl von Bytes im Puffer. Übergeben Sie D3DX DEFAULT, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie \_ die Größenüberprüfung überspringen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
