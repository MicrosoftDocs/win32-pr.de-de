---
title: "\"Undvtaskplugin\"-Starttask-Methode"
description: Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Starttask-Methode Remotedesktopdienste
- Starttask-Methode Remotedesktopdienste, undvtaskplugin-Schnittstelle
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, Starttask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477427"
---
# <a name="irdvtaskpluginstarttask-method"></a>Undvtaskplugin:: Starttask-Methode

Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.

## <a name="syntax"></a>Syntax


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Bezeichnung* \[ in\]
</dt> <dd>

Die Bezeichnung für den Task. Dies ist die Bezeichnung, die in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurde.

</dd> <dt>

*Bezeichner* \[ in\]
</dt> <dd>

Der Bezeichner des Tasks. Dies ist der Bezeichner, der in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurde.

</dd> <dt>

*Kontext* \[ in\]
</dt> <dd>

Optionale Daten für den Task. Dies sind die Daten, die in der [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) -Methode an den Auslöse-Agent übergeben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Undvtaskplugin"**](irdvtaskplugin.md)
</dt> </dl>

 

 





