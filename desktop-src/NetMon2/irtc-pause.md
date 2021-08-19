---
description: 'IRTC::P ause-Methode: Die Pause-Methode hält die aktuelle Erfassung an.'
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC::P ause-Methode (Netmon.h)
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
ms.openlocfilehash: 1ad7ce342c1e0053622bfb77161ecd1e5d81c25d09af179108065b445dd4dc35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365075"
---
# <a name="irtcpause-method"></a>IRTC::P ause-Methode

Die **Pause-Methode** hält die aktuelle Erfassung an.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung wurde bereits angehalten.<br/>                                                                                     |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl>  | Der NPP erfasst keine Daten. Rufen Sie [IRTC::Start auf,](irtc-start.md) um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Verbinden](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Während sich die Erfassung im angehaltenen Zustand befindet, werden neue Frames erst erfasst, wenn die [IRTC::Resume-Methode](irtc-resume.md) aufgerufen wird, um die Erfassung neu zu starten.

Wenn Sie die **Methoden IRTC::P ause** und **IRTC::Resume** verwenden, um die Erfassung [](c.md) zu steuern, fügt Netzwerkmonitor weiterhin Konversationsstatistiken hinzu, wenn die Erfassung ausgeführt wird.

Rufen Sie [IRTC::Resume](irtc-resume.md)auf, um den Erfassungsaufruf neu zu starten. Rufen Sie [IRTC::Stop](irtc-stop.md)auf, um die Erfassung zu beenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




