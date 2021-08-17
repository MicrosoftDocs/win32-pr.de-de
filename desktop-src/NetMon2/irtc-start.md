---
description: Die Start-Methode startet die Erfassung.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: IRTC::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 17ccb07a97112cab4390dc1eece2bf6fce51acf1c80244ed03253b5a2f6112b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132919"
---
# <a name="irtcstart-method"></a>IRTC::Start-Methode

Die **Start-Methode** startet die Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                           | Beschreibung                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl> | Die Erfassung befindet sich in einem angehaltenen Zustand und muss beendet werden, bevor sie neu gestartet werden kann. Rufen Sie [IRTC::Stop auf,](idelaydc-stop.md) um die Erfassung zu beenden.<br/> |
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>       | Die Erfassung wurde bereits gestartet.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>  | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Verbinden](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/>                         |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                                             |



 

## <a name="remarks"></a>Hinweise

Wenn Sie die Erfassung mithilfe der Methoden IRTC::Start und [IRTC::Stop](irtc-stop.md) neu starten, müssen Sie die [IRTC::Configure-Methode](irtc-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie IRTC::Start aufrufen, um die Datenerfassung neu zu starten.

> [!Note]  
> Sie können die Erfassung auch mithilfe der [Methoden IRTC::P ause](irtc-pause.md) und [IRTC::Resume](irtc-resume.md) starten und beenden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Resume](irtc-resume.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




