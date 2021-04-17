---
title: Iconnectionbrokerclient-Schnittstelle (cbclient. h)
description: Stellt die Methoden bereit, die zum Verwenden des Remotedesktopverbindung Broker-Clients erforderlich sind.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478891"
---
# <a name="iconnectionbrokerclient-interface"></a>Iconnectionbrokerclient-Schnittstelle

Stellt die Methoden bereit, die zum Verwenden des Remotedesktopverbindung Broker-Clients erforderlich sind.

Diese Schnittstelle wird vom System implementiert. Verwenden Sie die [**cbkreateclientinstance**](cbcreateclientinstance.md) -Funktion, um eine Instanz dieser Schnittstelle abzurufen.

## <a name="members"></a>Member

Die **iconnectionbrokerclient** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iconnectionbrokerclient** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iconnectionbrokerclient** -Schnittstelle verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Gettargetinfo**](iconnectionbrokerclient-gettargetinfo.md) | Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Header<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ iconnectionbrokerclient ist als D6818DF2-8338-4EB7-AD77-DE210817987C definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbkreateclientinstance**](cbcreateclientinstance.md)
</dt> </dl>

 

