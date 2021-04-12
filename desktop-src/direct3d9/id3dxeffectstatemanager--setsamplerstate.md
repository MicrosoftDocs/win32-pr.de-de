---
description: Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'ID3DXEffectStateManager:: setsamplerstate-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355177"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a>ID3DXEffectStateManager:: setsamplerstate-Methode

Eine Rückruffunktion, die von einem Benutzer implementiert werden muss, um einen Sampler festzulegen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sampler* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Die null basierte samplernummer.

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Typ: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**

Identifiziert den samplerstatus, der die Filterung, Adressierung oder die Rahmenfarbe angeben kann. Siehe [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Ein Wert von einem der samplerstatustypen im-Typ.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn der Rückruf beim Festlegen des Geräte Zustands fehlschlägt, wird eine der folgenden Aktionen ausgeführt:

-   Der Effekt schlägt während [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md)fehl.
-   Der Status des dynamischen Effekts (z. b. [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) schlägt fehl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
