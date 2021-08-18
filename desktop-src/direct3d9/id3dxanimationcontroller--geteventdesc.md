---
description: Ruft eine Beschreibung eines angegebenen Animationsereignisses ab.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: ID3DXAnimationController::GetEventDesc-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc113788a8eb6b64accfcba8c58dd3a3512e17601ec02ce5dd33349628c69212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987940"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>ID3DXAnimationController::GetEventDesc-Methode

Ruft eine Beschreibung eines angegebenen Animationsereignisses ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hEvent* \[ In\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignishandle für ein zu beschreibende Animationsereignis.

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**

Zeiger auf eine [**D3DXEVENT \_ DESC-Struktur,**](d3dxevent-desc.md) die eine Beschreibung des Animationsereignisses enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




