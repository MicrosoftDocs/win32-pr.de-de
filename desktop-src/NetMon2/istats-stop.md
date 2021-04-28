---
description: 'IStats::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: IStats::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114608"
---
# <a name="istatsstop-method"></a>IStats::Stop-Methode

Die **Stop-Methode** beendet die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl>   | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [die IStats::Connect-Methode auf,](istats-connect.md) um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl>   | Der NPP erfasst keine Daten. Rufen Sie die [IStats::Start-Methode auf,](istats-start.md) um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ NUR STATISTIKEN \_**</dt> </dl> | Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IStats::Connect-Methode.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Bemerkungen

Stellen Sie beim Neustarten der Erfassung nach dem Aufruf von **IStats::Stop** sicher, dass Sie jedes Mal die [IStats::Configure-Methode](istats-configure.md) aufrufen, wenn Sie [IStats::Start](istats-start.md) aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Connect](istats-connect.md)
</dt> <dt>

[IStats::Configure](istats-configure.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> </dl>

 

 




