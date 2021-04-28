---
description: 'ID3DXRenderToEnvMap::OnResetDevice-Methode: Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.'
ms.assetid: 3e231ad6-858e-4b6a-bbea-0839794bbac7
title: ID3DXRenderToEnvMap::OnResetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78b9e6e1081abed40d1eaf09f6540ed11ed119a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093128"
---
# <a name="id3dxrendertoenvmaponresetdevice-method"></a>ID3DXRenderToEnvMap::OnResetDevice-Methode

Verwenden Sie diese Methode, um Ressourcen erneut zu beziehen und den Anfangszustand zu speichern.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

**ID3DXRenderToEnvMap::OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird (mit [**IDirect3DDevice9::Reset),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)bevor andere Methoden aufgerufen werden. Dies ist ein guter Ort zum erneuten Abrufen von Videospeicherressourcen und Erfassen von Zustandsblöcken.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
