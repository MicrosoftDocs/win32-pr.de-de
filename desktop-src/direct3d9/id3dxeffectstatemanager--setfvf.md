---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager:: setf VF-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355210"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>ID3DXEffectStateManager:: setf VF-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen FVF-Code festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*F-VF* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die FVF-Konstante, die bestimmt, wie Scheitelpunkt Daten interpretiert werden. Siehe [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der dynamische Effekt Zustands Aufrufe (z. b. [**IDirect3DDevice9:: setfvf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
