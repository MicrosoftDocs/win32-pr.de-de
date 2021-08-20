---
title: INapEnforcementClientConnection2-Schnittstelle (NapEnforcementClient.h)
description: Clientverbindungsverwaltung zulassen. | INapEnforcementClientConnection2-Schnittstelle (NapEnforcementClient.h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2-Schnittstelle NAP
- INapEnforcementClientConnection2-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: e60e91ffbc12534bb3b5a8ac22cbd13a1238ba32e09b4f56b4ab570ffd1ea8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144393"
---
# <a name="inapenforcementclientconnection2-interface"></a>INapEnforcementClientConnection2-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**INapEnforcementClientConnection2** stellt Methoden bereit, die die Verwaltung von Clientverbindungen ermöglichen.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapEnforcementClientConnection2-Schnittstelle** erbt von [**INapEnforcementClientConnection**](inapenforcementclientconnection.md). **INapEnforcementClientConnection2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapEnforcementClientConnection2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                              | Beschreibung                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Wird verwendet, um die IDs der installierten SHVs für den Client abzurufen.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Wird verwendet, um die Isolationsinformationen für den Client abzurufen.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Wird vom NapAgent verwendet, um die installierten SHV-IDs für den Client festzulegen.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Wird vom NapAgent verwendet, um die Isolationsinformationen für den Client festzulegen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





