---
description: Empfängt IShellWindows-Fensterregistrierungsereignisse.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: DShellWindowsEvents-Objekt (Exdisp.h)
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
ms.openlocfilehash: 13335268b892e4ac95520221fcd2e413c9c255225ccd8fc36c3c73cbf8c327a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009540"
---
# <a name="dshellwindowsevents-object"></a>DShellWindowsEvents-Objekt

Empfängt [**IShellWindows-Fensterregistrierungsereignisse.**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)

## <a name="members"></a>Member

Das **DShellWindowsEvents-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **DShellWindowsEvents-Objekt** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Wird aufgerufen, wenn die Registrierung eines Shellfensters widerrufen wird. <br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden **Sie DShellWindowsEvents,** um zu überwachen, wann ein Shellfenster registriert oder widerrufen wird. Weitere Informationen finden Sie unter [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Product (Produkt)<br/> | Internet Explorer 5<br/>                                                                                           |
| Header<br/>  | <dl> <dt>Exdisp.h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




