---
title: AxWindowsMediaPlayer. openstate (Eigenschaft)
description: Die openstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- openstate-Eigenschaften Fenster Media Player
- openstate-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, openstate (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357990"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>AxWindowsMediaPlayer. openstate (Eigenschaft)

Die openstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>Eigenschaftswert

Der WMPLib. wmpopenstate-Enumerationswert.

## <a name="remarks"></a>Bemerkungen

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. OpenStateChange-Ereignis**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib. wmpopenstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





