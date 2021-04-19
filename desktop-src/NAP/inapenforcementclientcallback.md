---
title: Inapenforcementclientcallback-Schnittstelle (napforcementclient. h)
description: Erzwingungs Clients müssen implementieren, damit der NAPAgent mit Ihnen kommunizieren kann.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- Inapenforcementclientcallback-Schnittstelle NAP
- Inapenforcementclientcallback-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342486"
---
# <a name="inapenforcementclientcallback-interface"></a>Inapenforcementclientcallback-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientcallback** -Schnittstelle stellt Rückruf Methoden bereit, die von Erzwingungs Clients implementiert werden müssen, damit der NAPAgent mit Ihnen kommunizieren kann.

## <a name="members"></a>Member

Die **inapenforcementclientcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapenforcementclientcallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapenforcementclientcallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**Inapenforcementclientcallback:: GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Wird vom NAPAgent zum Abrufen von Verbindungen verwendet.<br/>                         |
| [**Inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md) | Wird vom NAPAgent verwendet, um den Erzwingungs Client über SoH-Änderungen zu informieren.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |



 

