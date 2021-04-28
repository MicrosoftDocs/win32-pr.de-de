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
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103768"
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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IESP::Connect](iesp-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl> | Das NPP erfasst keine Daten. Rufen Sie [IESP::Start](iesp-start.md) auf, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NOT \_ ESP**</dt> </dl>       | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IESP::Connect-Methode.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn die **IESP::Stop-Methode** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungsdatei.*](c.md) (Der Name der Erfassungsdatei wurde zurückgegeben, als [IESP::Start](iesp-start.md) aufgerufen wurde.) Sie können sich nun den Inhalt der Aufzeichnungsdatei ansehen.

Wenn Sie die Erfassung beenden und neu starten, müssen Sie jedes Mal die [IESP::Configure-Methode](iesp-configure.md) aufrufen, wenn Sie [IESP::Start](iesp-start.md) aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




