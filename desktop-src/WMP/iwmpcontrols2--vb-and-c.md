---
title: IWMPControls2 (VB und C )-Schnittstelle (Wmp.h)
description: Stellt eine Methode bereit, die die iwmpcontrols-Schnittstelle ergänzt.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB und C) Interface Windows Media Player
- IWMPControls2 (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351323"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>IWMPControls2-Schnittstelle (VB und c#)

Stellt eine Methode bereit, die die [**iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) -Schnittstelle ergänzt.

## <a name="members"></a>Member

Die IWMPControls2-Schnittstelle **(VB und c#)** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die IWMPControls2-Schnittstelle **(VB und c#)** verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Schritt**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Verschiebt das aktuelle Video Medien Element in den nächsten Frame oder den vorherigen Frame und friert die Wiedergabe.<br/> |



 

Der folgende Beispielcode zeigt, wie auf eine [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) -Schnittstelle zugegriffen wird. Im Beispielcode wird der [**iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) -Wert umgewandelt, der von der [**AxWindowsMediaPlayer. ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) -Eigenschaft an einen **IWMPControls2** -Wert zurückgegeben wird.

Für **c#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Für **VB**:


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcontrols**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Iwmpcontrols-Schnittstelle (VB und c#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls3-Schnittstelle (VB und c#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





