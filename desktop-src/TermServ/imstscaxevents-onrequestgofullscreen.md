---
title: IMsTscAxEvents OnRequestGoFullScreen-Methode
description: Wird aufgerufen, wenn der Client den Wechsel in den Vollbildmodus an fordert und die Methode IMsTscAdvancedSettings put ContainerHandledFullScreen aufgerufen wird, um die ContainerHandledFullScreen-Eigenschaft auf einen Wert ungleich 0 (null) zu \_ setzen.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- OnRequestGoFullScreen-Remotedesktopdienste
- OnRequestGoFullScreen-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRequestGoFullScreen-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6d689469f635694357890c620866fff5783680f8e9e8d11a1a05c78f6e1e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770680"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a>IMsTscAxEvents::OnRequestGoFullScreen-Methode

Wird aufgerufen, wenn der Client den Wechsel in den Vollbildmodus an fordert, und die [**Methode IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) aufgerufen wird, um die **ContainerHandledFullScreen-Eigenschaft** auf einen Wert ungleich 0 (null) zu setzen.

## <a name="syntax"></a>Syntax


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Im vollbildbasierten Containermodus sollte der Container als Reaktion auf dieses Ereignis in den Vollbildmodus "Standard" wechseln.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Requirements for Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





