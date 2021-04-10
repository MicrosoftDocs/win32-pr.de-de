---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager:: setnpatchmode-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961752"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a>ID3DXEffectStateManager:: setnpatchmode-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um die Anzahl der unter Divisions Segmente für N-Patches festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*nsegmente* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Unterteilen Sie die Oberfläche in diese Anzahl von Unterteilungen. Dies entspricht der Anzahl, die von [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der dynamische Effekt Status-aufrufen (z. b. [**IDirect3DDevice9:: setnpatchmode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
