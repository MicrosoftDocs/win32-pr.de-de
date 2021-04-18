---
title: Iremotedesktopclientevents-Methode (onadminmessagereceived)
description: Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Onadminmessagereceived-Methode Remotedesktopdienste
- Onadminmessagereceived-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onadminmessagereceived-Methode
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
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392071"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a>Iremotedesktopclientevents:: onadminmessagereceived-Methode

Wird aufgerufen, wenn das Client Steuerelement eine administrative Nachricht empfängt.

## <a name="syntax"></a>Syntax


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AdminMessage* \[ in\]
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
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclientevents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





