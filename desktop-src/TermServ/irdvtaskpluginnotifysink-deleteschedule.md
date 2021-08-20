---
title: IRDVTaskPluginNotifySink DeleteSchedule-Methode
description: Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- DeleteSchedule-Methode Remotedesktopdienste
- DeleteSchedule-Methode Remotedesktopdienste , IRDVTaskPluginNotifySink-Schnittstelle
- IRDVTaskPluginNotifySink-Schnittstelle Remotedesktopdienste , DeleteSchedule-Methode
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5674b3624edc102be6943e63b72444ec68f403fa1066e90a410f028008894d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129142"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>IRDVTaskPluginNotifySink::D eleteSchedule-Methode

Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrIdentifier* \[ In\]
</dt> <dd>

Der Bezeichner des geplanten Tasks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





