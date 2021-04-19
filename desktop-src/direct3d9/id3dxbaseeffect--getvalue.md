---
description: Den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen, erhalten. Diese Methode kann anstelle von fast allen GetXXX-aufrufen in ID3DXBaseEffect verwendet werden.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: 'ID3DXBaseEffect:: GetValue-Methode (D3DX9Shader. h)'
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
ms.openlocfilehash: 166635b22875692da0396f1c7c2145f13ca08df3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363956"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>ID3DXBaseEffect:: GetValue-Methode

Den Wert eines beliebigen Parameters oder einer Anmerkung, einschließlich einfacher Typen, Strukturen, Arrays, Zeichen folgen, Shader und Texturen, erhalten. Diese Methode kann anstelle von fast allen GetXXX-aufrufen in [**ID3DXBaseEffect**](id3dxbaseeffect.md)verwendet werden.

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

*hparameter* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Gibt einen Puffer zurück, der den Wert enthält.

</dd> <dt>

*Bytes* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

\[gibt \] die Anzahl der Bytes im Puffer an. Übergeben Sie D3DX \_ Default, wenn Sie wissen, dass der Puffer groß genug ist, um den gesamten Parameter zu enthalten, und Sie die Größenüberprüfung überspringen möchten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
