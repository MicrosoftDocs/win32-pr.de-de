---
description: Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect:: SetValue-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132369"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>ID3DXBaseEffect:: SetValue-Methode

Legen Sie den Wert eines beliebigen Parameters oder einer Anmerkung fest, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen.

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

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der Daten enthält.

</dd> <dt>

*Bytes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

\[gibt \] die Anzahl der Bytes im Puffer an. Übergeben Sie D3DX \_ Default, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie die Größenüberprüfung überspringen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann anstelle von fast allen Effekten Satz-API-Aufrufen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
