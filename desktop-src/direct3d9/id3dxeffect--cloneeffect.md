---
description: Erstellt eine Kopie eines Effekts.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: ID3DXEffect::CloneEffect-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab5ebe2898c1525d3a539121d1e57708c4713df3a06b43bfa41572f0e7b23b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494260"
---
# <a name="id3dxeffectcloneeffect-method"></a>ID3DXEffect::CloneEffect-Methode

Erstellt eine Kopie eines Effekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das gerät darstellt, das dem Effekt zugeordnet ist.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Zeiger auf eine [**ID3DXEffect-Schnittstelle,**](id3dxeffect.md) die den geklonten Effekt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Funktion klont keinen Effekt, wenn der Benutzer während der Erstellung der Auswirkung [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md) angibt.

 

Informationen zum Aktualisieren freigegebener und nicht freigegebener Parameter in einer aktiven Technik eines geklonten Effekts finden Sie unter [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
