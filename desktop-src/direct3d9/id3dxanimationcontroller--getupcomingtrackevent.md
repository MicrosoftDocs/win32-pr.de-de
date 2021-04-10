---
description: Gibt ein Ereignis Handle für das nächste Ereignis zurück, das geplant ist, nachdem ein bestimmtes Ereignis auf einem Animations Titel auftritt.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'ID3DXAnimationController:: getupcomingtrackevent-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961558"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a>ID3DXAnimationController:: getupcomingtrackevent-Methode

Gibt ein Ereignis Handle für das nächste Ereignis zurück, das geplant ist, nachdem ein bestimmtes Ereignis auf einem Animations Titel auftritt.

## <a name="syntax"></a>Syntax


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Nach *verfolgen* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Bezeichner nachverfolgen.

</dd> <dt>

*hevent* \[ in\]
</dt> <dd>

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für ein angegebenes Ereignis, nach dem nach einem folgenden Ereignis gesucht werden soll. Wenn der Wert auf **null** festgelegt wird, gibt die Methode das nächste geplante Ereignis zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Ereignis Handle für das nächste Ereignis, das für die Ausführung auf dem angegebenen Track geplant ist. **Null** wird zurückgegeben, wenn kein neues Ereignis geplant ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann iterativ verwendet werden, um ein gewünschtes Ereignis durch wiederholtes übergeben von **null** für hevent zu suchen.

> [!Note]  
> Iterieren Sie nicht weiter, nachdem die Methode **null** zurückgegeben hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
