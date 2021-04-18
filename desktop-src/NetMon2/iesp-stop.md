---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP:: stopmethode (Netmon. h)'
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
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345477"
---
# <a name="iespstop-method"></a>IESP:: Station-Methode

Die Methode " **Beenden** " beendet die aktuelle Erfassung.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpstats* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [Statistik](statistics.md) Struktur, die Netzwerk Statistiken enthält, z. b. Gesamtrahmen und erfasste Bytes insgesamt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl> | Der NPP erfasst keine Daten. Wenden Sie [iESP:: Start](iesp-start.md) an, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>       | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn die **iESP:: Stopp** -Methode aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungs Datei.*](c.md) (Der Name der Erfassungs Datei wurde zurückgegeben, als " [iESP:: Start](iesp-start.md) " aufgerufen wurde.) Nun können Sie sich den Inhalt der Erfassungs Datei ansehen.

Wenn Sie die Erfassung beenden und neu starten, stellen Sie sicher, dass Sie bei jedem Aufruf von [iESP:: Start](iesp-start.md) die Methode [iESP:: Configure](iesp-configure.md) aufruft, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[Kam](statistics.md)
</dt> </dl>

 

 




