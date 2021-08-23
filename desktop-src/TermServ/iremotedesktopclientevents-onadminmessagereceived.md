---
title: IRemoteDesktopClientEvents OnAdminMessageReceived-Methode
description: Wird aufgerufen, wenn das Clientsteuer steuerelement eine Administratornachricht empfängt.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- OnAdminMessageReceived-Remotedesktopdienste
- OnAdminMessageReceived-Methode Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnAdminMessageReceived-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6c50b4b3f26564cc93f1e41653e856f2984559234de92dd2ed2ab02bee20cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511890"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a>IRemoteDesktopClientEvents::OnAdminMessageReceived-Methode

Wird aufgerufen, wenn das Clientsteuer steuerelement eine Administratornachricht empfängt.

## <a name="syntax"></a>Syntax


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*adminMessage* \[ In\]
</dt> <dd>

Die Meldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





