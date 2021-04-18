---
description: 'Eine Anwendung implementiert diese Schnittstelle, um Rückrufe in Animations Sätzen zu verarbeiten, die durch Aufrufe von ID3DXAnimationController:: AdvanceTime generiert werden.'
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: ID3DXAnimationCallbackHandler-Schnittstelle (D3dx9anim. h)
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
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371945"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>ID3DXAnimationCallbackHandler-Schnittstelle

Eine Anwendung implementiert diese Schnittstelle, um Rückrufe in Animations Sätzen zu verarbeiten, die durch Aufrufe von [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md)generiert werden.

## <a name="members"></a>Member

Die **ID3DXAnimationCallbackHandler** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DXAnimationCallbackHandler** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DXAnimationCallbackHandler** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Lenker Rückruf**](id3dxanimationcallbackhandler--handlecallback.md) | Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn ein Rückruf für einen Animations Satz in einer der-Spuren während eines Aufrufs von [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md)auftritt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der LPD3DXANIMATIONCALLBACKHANDLER-Typ wird als Zeiger auf diese Schnittstelle definiert.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
