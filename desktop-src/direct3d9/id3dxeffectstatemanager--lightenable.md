---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager:: lightenable-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219598"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a>ID3DXEffectStateManager:: lightenable-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um ein Licht zu aktivieren bzw. zu deaktivieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Der null basierte Index des Lichts. Dies ist derselbe Index in [**IDirect3DDevice9:: setlight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*Aktivieren* \[ von in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

True, wenn das Licht aktiviert werden soll, andernfalls false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der Aufruf des dynamischen Effekts-Zustands (z. [**b. IDirect3DDevice9:: lightenable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
