---
title: IMsTscAxEvents OnRequestContainerMinimize-Methode
description: Wird aufgerufen, wenn der Benutzer die Schaltfläche Minimieren auf der Verbindungsleiste im Vollbildmodus drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, die die Containeranwendung selbst minimiert.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- OnRequestContainerMinimize-Methode Remotedesktopdienste
- OnRequestContainerMinimize-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnRequestContainerMinimize-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125060"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>IMsTscAxEvents::OnRequestContainerMinimize-Methode

Wird aufgerufen, wenn der Benutzer die Schaltfläche **Minimieren** auf der Verbindungsleiste im Vollbildmodus drückt. Das Auslösen dieses Ereignisses ist eine Anforderung, die die Containeranwendung selbst minimiert.

## <a name="syntax"></a>Syntax


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird nur aufgerufen, wenn der containerverwendete Vollbildmodus aktiviert ist. Weitere Informationen finden Sie unter [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen.**](imstscadvancedsettings-containerhandledfullscreen.md)

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

 

 





