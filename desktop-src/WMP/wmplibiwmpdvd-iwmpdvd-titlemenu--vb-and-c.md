---
title: Iwmpdvd-titlemenu-Methode
description: Die titlemenu-Methode beendet die Wiedergabe und zeigt das Titelmenü an.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- titlemenu-Methode, Windows-Media Player
- titlemenu-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, titlemenu-Methode
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
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367791"
---
# <a name="iwmpdvdtitlemenu-method"></a>Iwmpdvd:: titlemenu-Methode

Die **titlemenu** -Methode beendet die Wiedergabe und zeigt das Titelmenü an.

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

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so erstellt, dass die **iwmpdvd. topmenu** -Methode und die **titlemenu** -Methode dasselbe Menü öffnen. Die **titlemenu** -Methode ruft in der Regel das Titelmenü auf, aber Sie kann das oberste Menü aufrufen, wenn kein Titel Menü verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd. topmenu (VB und c#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





