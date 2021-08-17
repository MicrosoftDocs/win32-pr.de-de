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
ms.openlocfilehash: 285d26e4eb141904e8a1951e6e42d0df0ef5d9738e5849057bbfe1e0a978e0b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743000"
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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IRTC::Verbinden](irtc-connect.md) auf, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl> | Das NPP erfasst keine Daten. Rufen Sie [IRTC::Start](irtc-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Wenn Sie die Erfassung nach dem Aufruf der **IRTC::Stop-Methode** neu starten, müssen Sie immer dann [IRTC::Configure](irtc-configure.md) aufrufen, wenn Sie [IRTC::Start](irtc-start.md) aufrufen, um die Erfassung neu zu starten.

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

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::Configure](irtc-configure.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> </dl>

 

 




