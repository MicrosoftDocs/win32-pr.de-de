---
title: IWMPDVD titleMenu-Methode
description: Die titleMenu-Methode beendet die Wiedergabe und zeigt das Titelmenü an.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- titleMenu-Methode Windows Media Player
- titleMenu-Methode Windows Media Player , IWMPDVD-Schnittstelle
- IWMPDVD-Schnittstelle Windows Media Player , titleMenu-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff485cd09915ec9acb076d2c06a8aa28c3549bf6527495e5e32d4a01d483285a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000460"
---
# <a name="iwmpdvdtitlemenu-method"></a>IWMPDVD::titleMenu-Methode

Die **titleMenu-Methode** beendet die Wiedergabe und zeigt das Titelmenü an.

## <a name="syntax"></a>Syntax


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jede DVD wird anders erstellt. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so erstellt, dass die Methoden **IWMPDVD.topMenu** und **titleMenu** das gleiche Menü öffnen. Die **titleMenu-Methode** ruft normalerweise das Titelmenü auf, kann jedoch das obere Menü aufrufen, wenn kein Titelmenü verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.topMenu (VB und C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





