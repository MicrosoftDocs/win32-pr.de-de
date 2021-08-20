---
title: IRDVTaskPlugin StartTask-Methode
description: Wird aufgerufen, um die Updateaufgabe auf dem virtuellen Computer zu starten.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- StartTask-Remotedesktopdienste
- StartTask-Remotedesktopdienste , IRDVTaskPlugin-Schnittstelle
- IRDVTaskPlugin-Schnittstelle Remotedesktopdienste , StartTask-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e0bb9104ee1bbd3f0f6c2e8cc04b691205f2e40cb2221b79b5e9f251492a3a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129257"
---
# <a name="irdvtaskpluginstarttask-method"></a>IRDVTaskPlugin::StartTask-Methode

Wird aufgerufen, um die Updateaufgabe auf dem virtuellen Computer zu starten.

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

*Bezeichnung* \[ In\]
</dt> <dd>

Die Bezeichnung für den Task. Dies ist die Bezeichnung, die in der ScheduleTask-Methode an den [**Trigger-Agent übergeben**](irdvtaskpluginnotifysink-scheduletask.md) wurde.

</dd> <dt>

*Bezeichner* \[ In\]
</dt> <dd>

Der Bezeichner des Tasks. Dies ist der Bezeichner, der in der ScheduleTask-Methode an den [**Trigger-Agent übergeben**](irdvtaskpluginnotifysink-scheduletask.md) wurde.

</dd> <dt>

*Kontext* \[ In\]
</dt> <dd>

Optionale Daten für den Task. Dies sind die Daten, die in der ScheduleTask-Methode an den [**Trigger-Agent übergeben**](irdvtaskpluginnotifysink-scheduletask.md) wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





