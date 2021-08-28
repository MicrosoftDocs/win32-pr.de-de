---
title: IConnectionBrokerRequest-Schnittstelle (Cbclient.h)
description: Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen IConnectionBrokerClient GetTargetInfo-Methode erforderlich sind.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerRequest-Schnittstelle Remotedesktopdienste
- IConnectionBrokerRequest-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dfc858e16371ec44ef965722c0d37bd388b060ce4d7ce75adbd904074df03b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059138"
---
# <a name="iconnectionbrokerrequest-interface"></a>IConnectionBrokerRequest-Schnittstelle

Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen [**IConnectionBrokerClient::GetTargetInfo-Methode**](iconnectionbrokerclient-gettargetinfo.md) erforderlich sind.

Diese Schnittstelle wird vom System implementiert. Eine Instanz dieser Schnittstelle wird dem Aufrufer mit der [**IConnectionBrokerClient::GetTargetInfo-Methode**](iconnectionbrokerclient-gettargetinfo.md) bereitgestellt.

## <a name="members"></a>Member

Die **IConnectionBrokerRequest-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerRequest** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IConnectionBrokerRequest-Schnittstelle** verfügt über diese Methoden.



| Methode                                                      | Beschreibung                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) | Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IConnectionBrokerRequest ist als 25114427-ED5D-46A6-AF53-C62D33A4108E definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

