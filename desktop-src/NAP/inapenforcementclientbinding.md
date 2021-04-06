---
title: Inapenforcementclientbinding-Schnittstelle (napforcementclient. h)
description: Erzwingungs Clients verwenden, um mit dem NAPAgent zu kommunizieren.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Inapenforcementclientbinding-Schnittstelle NAP
- Inapenforcementclientbinding-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859286"
---
# <a name="inapenforcementclientbinding-interface"></a>Inapenforcementclientbinding-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**Inapenforcementclientbinding** stellt Methoden bereit, die von Erzwingungs Clients für die Kommunikation mit dem NAPAgent verwendet werden.

## <a name="members"></a>Member

Die **inapenforcementclientbinding** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapenforcementclientbinding** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapenforcementclientbinding** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inapenforcementclientbinding:: kreateconnetction**](inapenforcementclientbinding-createconnection-method.md)                   | Wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.<br/>                                                                                                                                                            |
| [**Inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Wird vom Erzwingungs Client verwendet, wenn er eine SoH-Anforderung für eine bestimmte Verbindung benötigt.<br/>                                                                                                                   |
| [**Inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Startet den NAPAgent-Dienst. Der Erzwingungs Client muss diese Methode aufrufen, bevor eine andere Methode dieser Schnittstelle aufgerufen wird.<br/>                                                                            |
| [**Inapenforcementclientbinding:: notifyconnectionstatedown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.<br/>                                                                                                                      |
| [**Inapenforcementclientbinding:: notifysohchangefailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeitet werden konnte.<br/> |
| [**Inapenforcementclientbinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Wird von Erzwingungs Clients immer dann verwendet, wenn Sie ein SoH-Response Data BLOB vom Erzwingungs Server erhalten.<br/>                                                                                                       |
| [**Inapenforcementclientbinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Schließt den NAPAgent-Dienst für diese Client Verbindung ab.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Alle APIs in dieser Schnittstelle geben RPC \_ E getrennt zurück, \_ Wenn der NAPAgent angehalten wird. Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

