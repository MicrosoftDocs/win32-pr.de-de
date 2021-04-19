---
title: Iwmpdvd-topmenu-Methode
description: Die topmenu-Methode beendet die Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- topmenu-Methoden Fenster Media Player
- topmenu-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, topmenu-Methode
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
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361690"
---
# <a name="iwmpdvdtopmenu-method"></a>Iwmpdvd:: topmenu-Methode

Die **topmenu** -Methode beendet die Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.

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

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so erstellt, dass die **topmenu** -und **iwmpdvd. titlemenu** -Methoden dasselbe Menü öffnen. Die **topmenu** -Methode ruft normalerweise das Top-Menü (oder das Stamm Menü) auf, aber es kann das Menü Titel aufrufen, wenn kein Stamm Menü verfügbar ist.

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

[**Iwmpdvd. titlemenu (VB und c#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





