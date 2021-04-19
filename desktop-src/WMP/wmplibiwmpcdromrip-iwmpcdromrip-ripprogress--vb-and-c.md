---
title: Iwmpcdromrip-ripprogress (Eigenschaft)
description: Die ripprogress-Eigenschaft ruft den CD-einreißen-Status als Prozentsatz ab.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- ripprogress-Eigenschaften Fenster Media Player
- ripprogress-Eigenschaften Fenster Media Player, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle Windows Media Player, ripprogress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373818"
---
# <a name="iwmpcdromripripprogress-property"></a>Iwmpcdromrip:: ripprogress (Eigenschaft)

Die **ripprogress** -Eigenschaft ruft den CD-einreißen-Status als Prozentsatz ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der der Fortschritts Wert ist. Die Statuswerte liegen im Bereich von 0 bis 100.

## <a name="remarks"></a>Bemerkungen

Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten rippingprozesses dar. Verwenden Sie zum Bestimmen des Status einer bestimmten Spur " [iwmpmedia. getiteminfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) " mit " **ripprogress** " als Attributnamen. Um den Index des aktuell ausgetauppten Titels abzurufen, nennen Sie iwmpwiedergabe. getiteminfo mit "currentriptrackindex" als Attribut Name.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromrip-Schnittstelle (VB und c#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> </dl>

 

 





