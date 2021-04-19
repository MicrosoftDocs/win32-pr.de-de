---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager:: setmaterial-Methode (D3DX9Effect. h)'
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
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363153"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>ID3DXEffectStateManager:: setmaterial-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um den Materialzustand festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmaterial* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DMATERIAL9**](d3dmaterial9.md) \***

Ein Zeiger auf den Materialzustand. Siehe [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
