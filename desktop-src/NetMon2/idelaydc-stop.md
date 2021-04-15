---
description: Die Methode "beenden" beendet die aktuelle Erfassung.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Idelta aydc:: stopmethode (Netmon. h)'
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484307"
---
# <a name="idelaydcstop-method"></a>Idelta aydc:: stopmethode

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



| Rückgabecode                                                                                          | Beschreibung                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl> | Der NPP erfasst keine Daten. Wenden Sie [idelta-DC:: Start](idelaydc-start.md) an, um die Erfassung zu starten.<br/>                            |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>   | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn **idelta aydc:: Stopp** aufgerufen wird, beendet Netzwerkmonitor die Erfassung von Daten und schließt die [*Erfassungs Datei*](c.md). (Der Name der Erfassungs Datei wurde zurückgegeben, als " [idelta aydc:: Start](idelaydc-start.md) " aufgerufen wurde). Nun können Sie sich den Inhalt der Erfassungs Datei ansehen.

Wenn Sie die Erfassung beenden und starten, stellen Sie sicher, dass Sie jedes Mal, wenn Sie [idelta aydc:: Start](idelaydc-start.md) aufgerufen haben, die [idelta-DC:: Configure](idelaydc-configure.md) -Methode aufruft, um die Erfassung neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Connect](idelaydc-connect.md)
</dt> <dt>

[Idelta aydc:: Configure](idelaydc-configure.md)
</dt> <dt>

[Idelta aydc:: Start](idelaydc-start.md)
</dt> <dt>

[Kam](statistics.md)
</dt> </dl>

 

 




