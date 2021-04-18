---
title: Player. markerhit-Ereignis
description: Das markerhit-Ereignis tritt auf, wenn ein Marker erreicht wird. | Player. markerhit-Ereignis
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player "markerhit-Ereignisfenster"
- Markerhit-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, markerhit-Ereignis
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372307"
---
# <a name="playermarkerhit-event"></a>Player. markerhit-Ereignis

Das **markerhit** -Ereignis tritt auf, wenn ein Marker erreicht wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Markernum* 
</dt> <dd>

**Zahl** (**Long**), die die Nummer der Markierung angibt, die getroffen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> </dl>

 

 





