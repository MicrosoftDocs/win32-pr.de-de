---
title: Iremotedesktopclientevents ontouchpointercurrsorverschote-Methode
description: Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die EventsEnabled-Eigenschaft auf true festgelegt ist.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Ontouchpointercursor-Methode Remotedesktopdienste
- Ontouchpointercurrsorverschoder Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, ontouchpointercurrsorverschote-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338336"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a>Iremotedesktopclientevents:: ontouchpointercurrsorverschote-Methode

Wird aufgerufen, wenn der Fingerabdruck Cursor verschoben wurde und die [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) -Eigenschaft auf true festgelegt ist.

## <a name="syntax"></a>Syntax


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* \[ in\]
</dt> <dd></dd> <dt>

*j* \[ in\]
</dt> <dd></dd> </dl>

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

 

