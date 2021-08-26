---
title: IRemoteDesktopClientEvents OnTouchPointerCursorMoved-Methode
description: Wird aufgerufen, wenn der Touchzeigercursor verschoben wurde und die EventsEnabled-Eigenschaft auf TRUE festgelegt ist.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- OnTouchPointerCursorMoved-Remotedesktopdienste
- OnTouchPointerCursorMoved-Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnTouchPointerCursorMoved-Methode
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
ms.openlocfilehash: 4a7c6d542031ab375d7e960b82bb36ba52ea6c9ecab58764c13595871687a731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072300"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a>IRemoteDesktopClientEvents::OnTouchPointerCursorMoved-Methode

Wird aufgerufen, wenn der Touchzeigercursor verschoben wurde und die [**EventsEnabled-Eigenschaft**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) auf TRUE festgelegt ist.

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

*y* \[ in\]
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
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

