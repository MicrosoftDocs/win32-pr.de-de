---
description: Empfängt IShellWindows-Fenster Registrierungs Ereignisse.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Dshellwindowsevents-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983013"
---
# <a name="dshellwindowsevents-object"></a>Dshellwindowsevents-Objekt

Empfängt [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) -Fenster Registrierungs Ereignisse.

## <a name="members"></a>Member

Das **dshellwindowsevents** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **dshellwindowsevents** -Objekt verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**Windowregistered**](dshellwindowsevents-windowregistered.md) | Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird. <br/> |
| [**Windows-gesperrt**](dshellwindowsevents-windowrevoked.md)       | Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **dshellwindowsvents** , um zu überwachen, wann ein Shellfenster registriert oder widerrufen wird. Weitere Informationen finden Sie unter [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produkt<br/> | Internet Explorer 5<br/>                                                                                           |
| Header<br/>  | <dl> <dt>Exdisp. h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shellwindows**](shellwindows.md)
</dt> </dl>

 

 




