---
description: Beenden eines aktiven Pass.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect:: endpass-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355007"
---
# <a name="id3dxeffectendpass-method"></a>ID3DXEffect:: endpass-Methode

Beenden eines aktiven Pass.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt immer den Wert S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung signalisiert das Ende des Renderings eines aktiven Pass durch Aufrufen von **ID3DXEffect:: endpass**. Jede **ID3DXEffect:: endpass** -Aktivität muss Teil eines übereinstimmenden Paars von [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) -und **ID3DXEffect:: endpass** -aufrufen sein.

Jedes übereinstimmende Paar aus [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) -und **ID3DXEffect:: endpass** -aufrufen muss sich innerhalb eines übereinstimmenden Paares von [**ID3DXEffect:: begin**](id3dxeffect--begin.md) -und [**ID3DXEffect:: End**](id3dxeffect--end.md) -aufrufen befinden.

Wenn die Anwendung in einem [](id3dxeffect.md) [**ID3DXEffect:: beginpass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: endpass** -übereinstimmenden paar den Effekt Zustand ändert, muss Sie [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) aufrufen, bevor ein drawxprimitiver-Aufrufvorgang Zustandsänderungen vor dem Rendering an das Gerät weitergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




