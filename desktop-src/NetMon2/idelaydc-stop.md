---
description: 'IDelaydC::Stop-Methode: Die Stop-Methode beendet die aktuelle Erfassung.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: IDelaydC::Stop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b5fb6442481574de6732aef1359cf9586b9cdcc1815d9f0b206a1f8a597f1967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366000"
---
# <a name="idelaydcstop-method"></a>IDelaydC::Stop-Methode

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



| Rückgabecode                                                                                          | Beschreibung                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IDelaydC::Verbinden](idelaydc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl> | Der NPP erfasst keine Daten. Rufen [Sie IDelaydC::Start auf,](idelaydc-start.md) um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IDelaydC::Verbinden-Methode.](idelaydc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Wenn **IDelaydC::Stop** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungsdatei*](c.md). (Der Name der Erfassungsdatei wurde zurückgegeben, als [IDelaydC::Start](idelaydc-start.md) aufgerufen wurde.) Sie können sich nun den Inhalt der Erfassungsdatei anzeigen lassen.

Wenn Sie die Erfassung beenden und starten, stellen Sie sicher, dass Sie jedes Mal, wenn Sie [IDelaydC::Start](idelaydc-start.md) aufrufen, die [IDelaydC::Configure-Methode](idelaydc-configure.md) aufrufen, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Verbinden](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




