---
description: 'IStats::Start-Methode: Die Start-Methode startet eine Erfassung.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: IStats::Start-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 494ec12a0bb9c5c312f34e9cc53e82bfcbe155f90c38b98b2ba807e9c87b6945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037150"
---
# <a name="istatsstart-method"></a>IStats::Start-Methode

Die **Start-Methode** startet eine Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ CAPTURE \_ PAUSED**</dt> </dl>  | Die Erfassung wurde angehalten und muss beendet werden, bevor sie neu gestartet werden kann. Rufen Sie die [IStats::Stop-Methode auf,](istats-stop.md) um die Erfassung zu beenden.<br/> |
| <dl> <dt>**NMERR-ERFASSUNG \_**</dt> </dl>        | Die Erfassung wurde bereits gestartet.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [die IStats::Verbinden-Methode](istats-connect.md) auf, um den NPP mit dem Netzwerk zu verbinden.<br/>           |
| <dl> <dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt> </dl> | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IStats::Verbinden-Methode.](istats-connect.md)<br/>                                          |



 

## <a name="remarks"></a>Hinweise

Wenn Sie die Erfassung mithilfe der Methoden IStats::Start und [IStats::Stop](istats-stop.md) neu starten, müssen Sie die [IStats::Configure-Methode](istats-configure.md) aufrufen, um die Verbindung jedes Mal neu zu konfigurieren, wenn Sie IStats::Start aufrufen, um die Datenerfassung neu zu starten.

> [!Note]  
> Sie können die Erfassung auch mithilfe der [Methoden IStats::P ause](istats-pause.md) und [IStats::Resume](istats-resume.md) starten und beenden. Wenn Sie diese Methoden verwenden, werden die erfassten Daten in derselben Erfassungsdatei gespeichert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Verbinden](istats-connect.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




