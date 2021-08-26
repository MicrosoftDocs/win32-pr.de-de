---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festlegen zu können.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: ID3DXEffectStateManager::SetFVF-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 828f6873ed9bf48de6a02d4195fdd1fa9d2bc39f99da1f8906fd8a2c53075cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026410"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>ID3DXEffectStateManager::SetFVF-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FVF* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die FVF-Konstante, die bestimmt, wie Scheitelpunktdaten interpretiert werden. Siehe [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetFVF)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
