---
title: INapComponentConfig2-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um eine Netzwerk Richtlinien Server-Benutzeroberfläche (NPS) Remote zu konfigurieren.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2-Schnittstelle NAP
- INapComponentConfig2 Interface NAP, beschrieben
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
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338329"
---
# <a name="inapcomponentconfig2-interface"></a>INapComponentConfig2-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapComponentConfig2** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um eine Netzwerk Richtlinien Server-Benutzeroberfläche (NPS) Remote zu konfigurieren.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**inapcomponentconfig**](inapcomponentconfig.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapComponentConfig2** -Schnittstelle erbt von [**inapcomponentconfig**](inapcomponentconfig.md). **INapComponentConfig2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentConfig2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                | BESCHREIBUNG                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2:: invokeuiformachine**](inapcomponentconfig2-invokeuiformachine.md)           | Wird von SHVs nach Bedarf implementiert, um die Remote Konfiguration direkt auf dem angegebenen Computer zu verwalten.<br/>                                                                 |
| [**INapComponentConfig2:: invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Wird von SHVs nach Bedarf implementiert, um die Konfiguration des Remote Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.<br/> |
| [**INapComponentConfig2:: isremoteconfigsupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Wird von SHVs implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.<br/>                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapcomponentconfig**](inapcomponentconfig.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





