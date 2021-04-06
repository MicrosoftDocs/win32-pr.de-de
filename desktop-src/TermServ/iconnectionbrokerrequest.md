---
title: Iconnectionbrokerrequest-Schnittstelle (cbclient. h)
description: Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen iconnectionbrokerclient gettargetinfo-Methode erforderlich sind.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste
- Iconnectionbrokerrequest-Schnittstelle Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743664"
---
# <a name="iconnectionbrokerrequest-interface"></a>Iconnectionbrokerrequest-Schnittstelle

Stellt die Methoden bereit, die zum Abrufen der Ergebnisse der asynchronen [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode erforderlich sind.

Diese Schnittstelle wird vom System implementiert. Eine Instanz dieser Schnittstelle wird dem Aufrufer mit der [**iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) -Methode bereitgestellt.

## <a name="members"></a>Member

Die **iconnectionbrokerrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iconnectionbrokerrequest** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iconnectionbrokerrequest** -Schnittstelle verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [**Check Status**](iconnectionbrokerrequest-checkstatus.md) | Wird aufgerufen, um den Status einer asynchronen Anforderung zu bestimmen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>     |
| IID<br/>                      | IID \_ iconnectionbrokerrequest ist als 25114427-ED5D-46a6-AF53-C62D33A4108E definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconnectionbrokerclient:: gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

