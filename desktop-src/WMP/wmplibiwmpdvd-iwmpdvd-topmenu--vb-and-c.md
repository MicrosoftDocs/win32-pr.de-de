---
title: IWMPDVD topMenu-Methode
description: Die topMenu-Methode beendet die Wiedergabe und zeigt das obere Menü (oder Stammmenü) für den aktuellen Titel an.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- topMenu-Windows Media Player
- topMenu-Methode Windows Media Player , IWMPDVD-Schnittstelle
- IWMPDVD-Schnittstelle Windows Media Player , topMenu-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f9cc1dcd528b93e9959f63a387747e510f7dd57b403ad70e41768d77006337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930212"
---
# <a name="iwmpdvdtopmenu-method"></a>IWMPDVD::topMenu-Methode

Die **topMenu-Methode** beendet die Wiedergabe und zeigt das obere Menü (oder Stammmenü) für den aktuellen Titel an.

## <a name="syntax"></a>Syntax


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jede DVD wird anders verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so verfasst, dass die **Methoden topMenu** und **IWMPDVD.titleMenu** das gleiche Menü öffnen. Die **topMenu-Methode** ruft in der Regel das obere Menü (oder Stammmenü) auf, kann jedoch das Titelmenü aufrufen, wenn kein Stammmenü verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB und C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





