---
title: INapEnforcementClientConnection2-Schnittstelle (napforcementclient. h)
description: Ermöglicht die clientverbindungsverwaltung. | INapEnforcementClientConnection2-Schnittstelle (napforcementclient. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2-Schnittstelle NAP
- INapEnforcementClientConnection2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869743"
---
# <a name="inapenforcementclientconnection2-interface"></a>INapEnforcementClientConnection2-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der **INapEnforcementClientConnection2** stellt Methoden bereit, die die Client Verbindungs Verwaltung ermöglichen.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapEnforcementClientConnection2** -Schnittstelle erbt von [**inapenforcementclientconnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapEnforcementClientConnection2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                              | BESCHREIBUNG                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2:: getinstalledshvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Wird verwendet, um die IDs der installierten SHVs für den Client abzurufen.<br/>             |
| [**INapEnforcementClientConnection2:: getisolationinfoex**](inapenforcementclientconnection2-getisolationinfoex.md) | Wird verwendet, um die Isolations Informationen für den Client zu erhalten.<br/>                 |
| [**INapEnforcementClientConnection2:: setinstalledshvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Wird von NAPAgent verwendet, um die installierten SHV-IDs für den Client festzulegen.<br/>     |
| [**INapEnforcementClientConnection2::/tisolationinfoex**](inapenforcementclientconnection2-setisolationinfoex.md) | Wird von NAPAgent verwendet, um die Isolations Informationen für den Client festzulegen.<br/> |



 

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

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





