---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der Unterteilungssegmente für N-Patches festlegen zu können.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: ID3DXEffectStateManager::SetNPatchMode-Methode (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 220d0541e6779ab1a3d4f3e189175abd7da82b1c8b7f378522d0c9df11896e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044428"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a>ID3DXEffectStateManager::SetNPatchMode-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der Unterteilungssegmente für N-Patches festlegen zu können.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nSegments* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Unterbricht die Oberfläche in diese Anzahl von Unterteilungen. Dies ist identisch mit der Zahl, die von [**IDirect3DDevice9::SetNPatchMode verwendet wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Gerätestatus fehlschlägt, tritt eine der folgenden Bedingungen auf:

-   Die Auswirkung tritt während [**ID3DXEffect::BeginPass auf.**](id3dxeffect--beginpass.md)
-   Der Dynamische Effektzustandsaufruf (z. B. [**IDirect3DDevice9::SetNPatchMode)**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)tritt ein Fehler auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
