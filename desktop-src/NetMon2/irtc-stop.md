---
description: 'IRTC::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: IRTC::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113518"
---
# <a name="irtcstop-method"></a>IRTC::Stop-Methode

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



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Connect auf,](irtc-connect.md) um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ WIRD NICHT \_ ERFASST**</dt> </dl> | Der NPP erfasst keine Daten. Rufen Sie [IRTC::Start auf,](irtc-start.md) um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Erfassung nach dem Aufruf der **IRTC::Stop-Methode** neu starten, müssen Sie jedes Mal [IRTC::Configure](irtc-configure.md) aufrufen, wenn Sie [IRTC::Start](irtc-start.md) aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




