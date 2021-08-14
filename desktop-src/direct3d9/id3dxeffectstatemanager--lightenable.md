---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren/zu deaktivieren.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: ID3DXEffectStateManager::LightEnable-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0a7ce5a4fe90e911faaf8927fe584004eec7a68eae7b5c75f1c3a92f017fd4bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295785"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a>ID3DXEffectStateManager::LightEnable-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren/zu deaktivieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der nullbasierte Index des Lichts. Dies ist derselbe Index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*Aktivieren* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

True, um das Licht zu aktivieren, andernfalls FALSE.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätezustands fehlschlägt, tritt eine der folgenden Schritte auf:

-   Die Auswirkung schlägt während [**id3DXEffect::BeginPass**](id3dxeffect--beginpass.md)fehl.
-   Der Dynamische Effektzustandsaufruf (z.B. [**IDirect3DDevice9::LightEnable)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
