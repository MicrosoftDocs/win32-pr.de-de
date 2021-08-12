---
title: IWMPControls2 (VB und C )-Schnittstelle (Wmp.h)
description: Stellt eine Methode bereit, die die IWMPControls-Schnittstelle ergänzt.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2-Schnittstelle (VB und C) Windows Media Player
- IWMPControls2-Schnittstelle (VB und C) Windows Media Player , beschrieben
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
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575920"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>IWMPControls2-Schnittstelle (VB und C#)

Stellt eine Methode bereit, die die [**IWMPControls-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) ergänzt.

## <a name="members"></a>Member

Die **IWMPControls2-Schnittstelle (VB und C#)** verfügt über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMPControls2-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Schritt**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Verschiebt das aktuelle Videomedienelement auf den nächsten Frame oder den vorherigen Frame und friert die Wiedergabe ein.<br/> |



 

Der folgende Beispielcode zeigt den Zugriff auf eine [**IWMPControls2-Schnittstelle.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) Im Beispielcode wird der [**IWMPControls-Wert,**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) den die [**AxWindowsMediaPlayer.Ctlcontrols-Eigenschaft**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) zurückgibt, in **einen IWMPControls2-Wert** um.

Für **C#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Für **VB:**


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPControls-Schnittstelle (VB und C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls3-Schnittstelle (VB und C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





