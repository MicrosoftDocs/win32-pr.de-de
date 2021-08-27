---
description: 'IESP::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: IESP::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d22333bcaad688fa9ebb805857db3673f48e70591e1d8953274598acef2b368b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037510"
---
# <a name="iespstop-method"></a>IESP::Stop-Methode

Die **Stop-Methode** beendet die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die Netzwerkstatistiken enthält, z. B. gesamt erfasste Frames und gesamt erfasste Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IESP::Verbinden](iesp-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl> | Der NPP erfasst keine Daten. Rufen [Sie IESP::Start auf,](iesp-start.md) um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ ESP**</dt> </dl>       | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IESP::Verbinden-Methode.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Wenn die **IESP::Stop-Methode** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungsdatei.*](c.md) (Der Name der Erfassungsdatei wurde zurückgegeben, als [IESP::Start](iesp-start.md) aufgerufen wurde.) Sie können sich nun den Inhalt der Erfassungsdatei anzeigen lassen.

Wenn Sie die Erfassung beenden und neu starten, müssen Sie jedes Mal, wenn Sie [IESP::Start](iesp-start.md) aufrufen, die [IESP::Configure-Methode](iesp-configure.md) aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Verbinden](iesp-connect.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




