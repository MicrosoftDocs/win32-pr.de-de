---
title: AxWindowsMediaPlayer.openState-Eigenschaft
description: Die openState-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- openState-Eigenschaft Windows Media Player
- openState-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , openState-Eigenschaft
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
ms.openlocfilehash: 09fa09451bf323a9f30afeddf7b2d003183a1eba7b0999a79fb42c70e1417013
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573570"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>AxWindowsMediaPlayer.openState-Eigenschaft

Die openState-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>Eigenschaftswert

Der WMPLib.WMPOpenState-Enumerationswert.

## <a name="remarks"></a>Hinweise

Windows Media Player Zustände werden in keiner bestimmten Reihenfolge garantiert. Darüber hinaus tritt nicht jeder Zustand notwendigerweise während einer Abfolge von Ereignissen auf. Sie sollten keinen Code schreiben, der von der Zustandsreihenfolge abhängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.OpenStateChange-Ereignis**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





