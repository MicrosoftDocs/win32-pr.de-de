---
description: Mit der Disconnect-Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Idelta-DC::D isconnect-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128336"
---
# <a name="idelaydcdisconnect-method"></a>Idelta-DC::D isconnect-Methode

Mit der **Disconnect** -Methode wird die Netzwerkverbindung mit dem Netzwerk getrennt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>      | Der NPP erfasst Daten. Sie können den NPP während einer Erfassung nicht vom Netzwerk trennen.<br/>            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden.<br/>                                                               |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>   | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann nicht aufgerufen werden, wenn der NPP Daten erfasst. Vor dem Aufrufen von **Disconnect** muss die **idelta-DC:: beenden** -Methode aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Connect](idelaydc-connect.md)
</dt> <dt>

[Idelta aydc:: Beendigung](idelaydc-stop.md)
</dt> </dl>

 

 




