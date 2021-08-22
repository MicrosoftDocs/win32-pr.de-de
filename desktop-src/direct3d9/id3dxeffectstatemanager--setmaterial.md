---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festlegen zu können.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: ID3DXEffectStateManager::SetMaterial-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 67e8b1ad498b5aacbae7aaad2d6b63fa406d54d6315a4e75b3028efe3107eaf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802874"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>ID3DXEffectStateManager::SetMaterial-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMaterial* \[ In\]
</dt> <dd>

Typ: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Ein Zeiger auf den Materialzustand. Siehe [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetMaterial)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
