---
description: Eine Anwendung implementiert diese Schnittstelle, um Rückrufe in Animationssätzen zu verarbeiten, die durch Aufrufe von ID3DXAnimationController::AdvanceTime generiert werden.
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: ID3DXAnimationCallbackHandler-Schnittstelle (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2eeec6fa26504d30588c5e148c07c6c628cc3ce752a2964d2dbefb3059040236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987980"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>ID3DXAnimationCallbackHandler-Schnittstelle

Eine Anwendung implementiert diese Schnittstelle, um Rückrufe in Animationssätzen zu verarbeiten, die durch Aufrufe von [**ID3DXAnimationController::AdvanceTime generiert werden.**](id3dxanimationcontroller--advancetime.md)

## <a name="members"></a>Member

Die **ID3DXAnimationCallbackHandler-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXAnimationCallbackHandler** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAnimationCallbackHandler-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HandleCallback**](id3dxanimationcallbackhandler--handlecallback.md) | Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn während eines Aufrufs von [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md)ein Rückruf für eine Animation auftritt, die in einer der Spuren festgelegt wurde.<br/> |



 

## <a name="remarks"></a>Hinweise

Der LPD3DXANIMATIONCALLBACKHANDLER-Typ ist als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
