---
description: Holen Sie sich den Effekt Zustands-Manager.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect:: GetStatus Manager-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371898"
---
# <a name="id3dxeffectgetstatemanager-method"></a>ID3DXEffect:: GetStatus Manager-Methode

Holen Sie sich den Effekt Zustands-Manager.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppManager* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Gibt einen Zeiger auf den Zustands-Manager zurück. Siehe [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) ist eine vom Benutzer implementierte Schnittstelle, die Rückrufe in eine Anwendung eingibt, um den Gerätezustand von einem Effekt festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: SetStatus Manager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




