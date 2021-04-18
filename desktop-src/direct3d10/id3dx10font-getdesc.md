---
description: Eine Beschreibung des aktuellen Schriftart Objekts erhalten.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font:: getdesc-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365117"
---
# <a name="id3dx10fontgetdesc-method"></a>ID3DX10Font:: getdesc-Methode

Eine Beschreibung des aktuellen Schriftart Objekts erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDE SC* \[ in\]
</dt> <dd>

Type: **[ **d3dx10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***

Zeiger auf eine [**d3dx10 \_ Font \_**](d3dx10-font-desc.md) -Debug-Struktur, die das Schriftart Objekt beschreibt. Wenn Unicode definiert ist, wird ein Zeiger auf einen D3DX10FONT- \_ descw zurückgegeben; andernfalls wird ein Zeiger auf einen D3DX10FONT \_ DeScA zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode beschreibt Unicode-Schriftart Objekte, wenn Unicode definiert ist. Andernfalls wird getdesca aufgerufen, wodurch ein Zeiger auf die D3DX10FONT DeScA-Struktur zurückgegeben wird \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




