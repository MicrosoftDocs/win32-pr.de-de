---
description: 'Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn ein Rückruf für einen Animations Satz in einer der-Spuren während eines Aufrufs von ID3DXAnimationController:: AdvanceTime auftritt.'
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'ID3DXAnimationCallbackHandler:: Lenker Callback-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360235"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>ID3DXAnimationCallbackHandler:: Lenker Callback-Methode

Die Anwendung implementiert diese Methode. Diese Methode wird aufgerufen, wenn ein Rückruf für einen Animations Satz in einer der-Spuren während eines Aufrufs von [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md)auftritt.

## <a name="syntax"></a>Syntax


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Bezeichner der Spur, auf der der Rückruf auftritt.

</dd> <dt>

*pcallbackdata* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Zeiger auf Benutzer eigene Rückruf Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
