---
description: Startet einen Durchlauf innerhalb der aktiven Technik.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect:: beginpass-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353367"
---
# <a name="id3dxeffectbeginpass-method"></a>ID3DXEffect:: beginpass-Methode

Startet einen Durchlauf innerhalb der aktiven Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Durchlauf* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein NULL basierter ganzzahliger Index in der Technik.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung legt einen aktiven Durchlauf (innerhalb eines aktiven Verfahrens) im Effektsystem fest, indem **ID3DXEffect:: beginpass** aufgerufen wird. Eine Anwendung signalisiert das Ende des aktiven Pass durch Aufrufen von [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md). **ID3DXEffect:: beginpass** und **ID3DXEffect:: endpass** müssen in einem übereinstimmenden Paar innerhalb eines übereinstimmenden Paares von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -aufrufen auftreten.

Wenn die Anwendung in einem [](id3dxeffect.md) **ID3DXEffect:: beginpass** / [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) -übereinstimmenden paar den Effekt Zustand ändert, muss Sie [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aufrufen, um das Update des Geräts mit den Statusänderungen festzulegen. Wenn keine Zustandsänderungen innerhalb eines **ID3DXEffect:: beginpass** -und **ID3DXEffect:: endpass** -übereinstimmenden Paars auftreten, ist es nicht erforderlich, **ID3DXEffect:: CommitChanges** aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
