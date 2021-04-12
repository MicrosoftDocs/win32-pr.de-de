---
description: Die Pause-Methode hält die aktuelle Erfassung an.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Untc::P ause-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215471"
---
# <a name="irtcpause-method"></a>Untc::P ause-Methode

Die **Pause** -Methode hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung \_ angehalten**</dt> </dl> | Die Erfassung wurde bereits angehalten.<br/>                                                                                     |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>  | Der NPP erfasst keine Daten. Wenden Sie zum Starten der Erfassung den Befehl " [irren:: Start](irtc-start.md) " an.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>  | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>   | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Während sich die Erfassung in einem angehaltenen Zustand befindet, werden neue Frames erst aufgezeichnet, wenn die Methode " [iritc:: Resume](irtc-resume.md) " aufgerufen wird, um die Erfassung neu zu starten.

Wenn Sie die Methode **IRTC::P ause** und **IRTC:: Resume** zum Steuern der Erfassung verwenden, werden Netzwerkmonitor weiterhin [*Konversations Statistiken*](c.md) hinzufügen, sobald die Erfassung ausgeführt wird.

Zum Neustarten des Aufzeichnungs Aufrufes " [untc:: Resume](irtc-resume.md)". Um die Erfassung zu verhindern, nennen Sie " [irren:: Ende](irtc-stop.md)".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

[Iran:: Resume](irtc-resume.md)
</dt> <dt>

["Iran:: Start"](irtc-start.md)
</dt> <dt>

[Iran:: Beendigung](irtc-stop.md)
</dt> </dl>

 

 




