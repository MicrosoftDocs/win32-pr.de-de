---
title: IRDVTaskPluginNotifySink ScheduleTask-Methode
description: Wird vom Task-Agent aufgerufen, um einen Task zu planen.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask-Remotedesktopdienste
- ScheduleTask-Remotedesktopdienste , IRDVTaskPluginNotifySink-Schnittstelle
- IRDVTaskPluginNotifySink-Schnittstelle Remotedesktopdienste , ScheduleTask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdcecba38b1fd5eb773e5076f5485ae900e5423267a3a311091bf01e0ed86ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512020"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>IRDVTaskPluginNotifySink::ScheduleTask-Methode

Wird vom Task-Agent aufgerufen, um einen Task zu planen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ftStartTime* \[ In\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Die früheste Startzeit der Aufgabe in UTC.

</dd> <dt>

*ftEndTime* \[ In\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Die Endzeit der Aufgabe in UTC. Übergeben Sie [**einen FILETIME-Wert,**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) der auf alle Nullen festgelegt ist, wenn keine Endzeit angegeben ist.

</dd> <dt>

*ftDeadline* \[ In\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Der Stichtag für die Aufgabe in UTC. Damit wird die Priorität für mehrere Aufgaben innerhalb ihres Startfensters festgelegt. Wenn mehr als eine Aufgabe gestartet werden soll, wird zuerst die Aufgabe mit dem frühesten Stichtag gestartet.

</dd> <dt>

*bstrLabel* \[ In\]
</dt> <dd>

Typ: **BSTR**

Die Bezeichnung für den Task. Dies wird an die [**StartTask-Methode**](irdvtaskplugin-starttask.md) übergeben.

</dd> <dt>

*bstrIdentifier* \[ In\]
</dt> <dd>

Typ: **BSTR**

Der Bezeichner des Tasks. Dies wird an die [**StartTask-Methode**](irdvtaskplugin-starttask.md) übergeben.

</dd> <dt>

*saContext* \[ In\]
</dt> <dd>

Typ: **SAFEARRAY(BYTE)**

Optionale Daten für den Task. Dies wird an die [**StartTask-Methode**](irdvtaskplugin-starttask.md) übergeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

