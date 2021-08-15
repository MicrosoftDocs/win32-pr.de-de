---
description: Animiert das Gitternetz und verläuft um einen angegebenen Wert für die globale Animationszeit.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: ID3DXAnimationController::AdvanceTime-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c11a3b356fb0f09cc3372db3ccebd824b4dc8290ff586eed9de3b9fa2ea13ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987960"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>ID3DXAnimationController::AdvanceTime-Methode

Animiert das Gitternetz und verläuft um einen angegebenen Wert für die globale Animationszeit.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TimeDelta* \[ In\]
</dt> <dd>

Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Der Betrag in Sekunden, um den die globale Animationszeit nach vorn geht. Der TimeDelta-Wert muss nicht negativ oder 0 (null) sein.

</dd> <dt>

*pCallbackHandler* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Zeiger auf eine benutzerdefinierte Benutzeroberfläche des Animationsrückrufhandlers [**ID3DXAnimationCallbackHandler.**](id3dxanimationcallbackhandler.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
