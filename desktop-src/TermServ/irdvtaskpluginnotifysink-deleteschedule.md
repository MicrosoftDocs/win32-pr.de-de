---
title: Undvtaskpluginnotifysink deleteschedule-Methode
description: Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Deleteschedule-Methode Remotedesktopdienste
- Deleteschedule-Methode Remotedesktopdienste, undvtaskpluginnotifysink-Schnittstelle
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, deleteschedule-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106167"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>Undvtaskpluginnotifysink::D eleteschedule-Methode

Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstridentifier* \[ in\]
</dt> <dd>

Der Bezeichner des geplanten Tasks.

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

[**"Undvtaskpluginnotifysink"**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





