---
title: Undvtaskpluginnotifysink ScheduleTask-Methode
description: Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask-Methode Remotedesktopdienste
- ScheduleTask-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, ScheduleTask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859247"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>Undvtaskpluginnotifysink:: ScheduleTask-Methode

Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.

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

*ftstarttime* \[ in\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Die früheste Startzeit der Aufgabe in UTC.

</dd> <dt>

"- *Zeit* \[ " in\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Die Endzeit der Aufgabe in UTC. Übergibt eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Menge auf alle Nullen, wenn keine Endzeit angegeben wird.

</dd> <dt>

*ftstichtag* \[ in\]
</dt> <dd>

Typ: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Der Task Stichtag in UTC. Hiermit wird die Priorität für mehrere Aufgaben festgelegt, die sich innerhalb des Start Fensters befinden. Wenn mehr als eine Aufgabe gestartet werden soll, wird die mit dem frühesten Stichtag zuerst gestartet.

</dd> <dt>

*bstraulabel* \[ in\]
</dt> <dd>

Typ: **BSTR**

Die Bezeichnung für den Task. Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.

</dd> <dt>

*bstridentifier* \[ in\]
</dt> <dd>

Typ: **BSTR**

Der Bezeichner des Tasks. Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.

</dd> <dt>

*sacontext* \[ in\]
</dt> <dd>

Typ: **SafeArray (Byte)**

Optionale Daten für den Task. Diese wird an die [**Starttask**](irdvtaskplugin-starttask.md) -Methode übermittelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Undvtaskpluginnotifysink"**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

