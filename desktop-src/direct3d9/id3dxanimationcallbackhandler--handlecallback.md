---
description: Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn während eines Aufrufs von ID3DXAnimationController::AdvanceTime ein Rückruf für eine Animation erfolgt, die in einer der Spuren festgelegt wurde.
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: ID3DXAnimationCallbackHandler::HandleCallback-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12fcfa0feba1d239cf72c37e78fec63140dda4f954e7c48dffd643dcca4400c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279210"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>ID3DXAnimationCallbackHandler::HandleCallback-Methode

Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn während eines Aufrufs von [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md)ein Rückruf für eine Animation auftritt, die in einer der Spuren festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nachverfolgen* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Bezeichner der Spur, auf der der Rückruf erfolgt.

</dd> <dt>

*pCallbackData* \[ In\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf Rückrufdaten im Besitz des Benutzers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR zurückgegeben wird.**](./d3dxerr.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
