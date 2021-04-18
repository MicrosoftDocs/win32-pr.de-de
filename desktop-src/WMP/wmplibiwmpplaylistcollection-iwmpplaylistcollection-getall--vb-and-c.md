---
title: Iwmpplaylistcollection GetAll-Methode
description: Die GetAll-Methode gibt eine iwmpplaylistarray-Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- GetAll-Methoden Fenster Media Player
- GetAll-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle, Windows Media Player, GetAll-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371210"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>Iwmpplaylistcollection:: GetAll-Methode

Die **GetAll** -Methode gibt eine **iwmpplaylistarray** -Schnittstelle zurück, die Zugriff auf alle Wiedergabelisten in der Bibliothek bietet.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmpplaylistarray** -Schnittstelle für das abgerufene Array von Wiedergabelisten.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9 oder höher.<br/>                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpplaylistarray-Schnittstelle (VB und c#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





