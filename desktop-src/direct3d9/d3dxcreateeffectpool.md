---
description: Erstellen Sie einen Effekt Pool. Ein Pool wird verwendet, um Parameter zwischen Effekten gemeinsam zu nutzen.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: D3DXCreateEffectPool-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219668"
---
# <a name="d3dxcreateeffectpool-function"></a>D3DXCreateEffectPool-Funktion

Erstellen Sie einen Effekt Pool. Ein Pool wird verwendet, um Parameter zwischen Effekten gemeinsam zu nutzen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pppool* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Gibt einen Zeiger auf den erstellten Pool zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.

Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ invalidcallzurück.

Wenn die Methode fehlschlägt, lautet der Rückgabewert E \_ Fail.

## <a name="remarks"></a>Bemerkungen

Für Effekte innerhalb eines Pools werden freigegebene Parameter mit dem gleichen Namen gemeinsam verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Funktionen](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




