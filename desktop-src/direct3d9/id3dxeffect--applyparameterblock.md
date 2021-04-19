---
description: Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.
ms.assetid: f228e2a2-64fa-4354-9f49-42d1d3b12d50
title: 'ID3DXEffect:: applyparameterblock-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.ApplyParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 12af672b929822180c4dba681ca333692a9174ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357237"
---
# <a name="id3dxeffectapplyparameterblock-method"></a>ID3DXEffect:: applyparameterblock-Methode

Wenden Sie die Werte in einem Zustands Block auf den Systemstatus aktueller Effekt an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyParameterBlock(
  [in] D3DXHANDLE  hParameterBlock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 *hparameterblock* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Ein Handle für den Parameter Block. Dies ist das Handle, das von [**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Erfassungs Effekt-Parameter Zustandsänderungen in einem Parameter Block durch Aufrufen von beginparameterblock; beendet die Erfassung von Zustandsänderungen, indem endparameterblock aufgerufen wird. Diese Zustandsänderungen beinhalten alle Auswirkung-Parameteränderungen, die in einer Technik auftreten (einschließlich der außerhalb eines bestanden). Wenn Sie mit dem Parameter Block abgeschlossen haben, können Sie deleteparameterblock aufrufen, um Arbeitsspeicher wiederherzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect:: beginparameterblock**](id3dxeffect--beginparameterblock.md)
</dt> <dt>

[**ID3DXEffect:: endparameterblock**](id3dxeffect--endparameterblock.md)
</dt> <dt>

[**ID3DXEffect::D eleteparameterblock**](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




