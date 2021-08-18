---
description: 'ID3DXFont::OnResetDevice-Methode: Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.'
ms.assetid: a63efb49-7864-4675-b367-4ae53995caea
title: ID3DXFont::OnResetDevice-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 37e09bab2473ace06b9e0fa803db523453ccff4796693d9faa1d410f5a6630f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748200"
---
# <a name="id3dxfontonresetdevice-method"></a>ID3DXFont::OnResetDevice-Methode

Verwenden Sie diese Methode, um Ressourcen erneut zu erhalten und den Anfangszustand zu speichern.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

**OnResetDevice** sollte jedes Mal aufgerufen werden, wenn das Gerät zurückgesetzt wird [**(mithilfe**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)von Reset ), bevor andere Methoden aufgerufen werden. Dies ist ein guter Ort zum erneuten Abrufen von Videospeicherressourcen und Erfassen von Zustandsblöcken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
