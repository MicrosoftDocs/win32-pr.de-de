---
title: IConnectionBrokerClient-Schnittstelle (Cbclient.h)
description: Stellt die Methoden zur Verwendung des Remotedesktopverbindung Broker-Clients zur Anwendung.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- IConnectionBrokerClient-Remotedesktopdienste
- IConnectionBrokerClient-Schnittstelle Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: a87c30729a5ec78e5275a6c2a1c0d9d139b857c3c7ea10f666ba09b7fceed256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059158"
---
# <a name="iconnectionbrokerclient-interface"></a>IConnectionBrokerClient-Schnittstelle

Stellt die Methoden zur Verwendung des Remotedesktopverbindung Broker-Clients zur Anwendung.

Diese Schnittstelle wird vom System implementiert. Um eine Instanz dieser Schnittstelle zu erhalten, verwenden Sie die [**CBCreateClientInstance-Funktion.**](cbcreateclientinstance.md)

## <a name="members"></a>Member

Die **IConnectionBrokerClient-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionBrokerClient** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IConnectionBrokerClient-Schnittstelle** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) | Fordert Informationen zum Zielcomputer an, auf dem die Verbindung umgeleitet werden soll.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Cbclient.lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IConnectionBrokerClient ist als D6818DF2-8338-4EB7-AD77-DE210817987C definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBCreateClientInstance**](cbcreateclientinstance.md)
</dt> </dl>

 

