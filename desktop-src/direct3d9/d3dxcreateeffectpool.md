---
description: Erstellen Sie einen Effektpool. Ein Pool wird verwendet, um Parameter zwischen Effekten freizugeben.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: D3DXCreateEffectPool-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 55df5e579b724a26e30223a0a0df7ffa815bda5a64b6f7d7e7e2c2c7f02f2fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804576"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool-Funktion

Erstellen Sie einen Effektpool. Ein Pool wird verwendet, um Parameter zwischen Effekten freizugeben.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppPool* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Gibt einen Zeiger auf den erstellten Pool zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.

Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ INVALIDCALL zurück.

Wenn die Methode fehlschlägt, ist der Rückgabewert E \_ FAIL.

## <a name="remarks"></a>Hinweise

Für Effekte innerhalb eines Pools teilen sich freigegebene Parameter mit demselben Namen Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effect-Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




