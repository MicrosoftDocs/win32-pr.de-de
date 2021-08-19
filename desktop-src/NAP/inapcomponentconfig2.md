---
title: INapComponentConfig2-Schnittstelle (NapCommon.h)
description: Stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit, um eine NPS-Benutzeroberfläche (Network Policy Server) remote zu konfigurieren.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2-Schnittstelle NAP
- INapComponentConfig2-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a80dfa1a9160b32b6d3c869795c9e23e41a5fdba39e38051bd29376caf8847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368377"
---
# <a name="inapcomponentconfig2-interface"></a>INapComponentConfig2-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapComponentConfig2-Schnittstelle** stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit, um eine Netzwerkrichtlinienserver-Benutzeroberfläche (NPS) remote zu konfigurieren.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapComponentConfig**](inapcomponentconfig.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapComponentConfig2-Schnittstelle** erbt von [**INapComponentConfig.**](inapcomponentconfig.md) **INapComponentConfig2** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentConfig2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                | Beschreibung                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Wird bei Bedarf von SHVs implementiert, um die Remotekonfiguration direkt auf dem angegebenen Computer zu verwalten.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Wird von SHVs nach Bedarf implementiert, um die Konfiguration des Remotecomputers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Wird von SHVs implementiert, um anzugeben, ob die Remotekonfiguration unterstützt wird.<br/>                                                                                      |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle sollte nicht von Systemzustands-Agents (SYSTEM Health Agents, SHAs) oder Quarantäneerzwingungsclients (QECs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





