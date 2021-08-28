---
title: INapServerInfo-Schnittstelle (NapServerManagement.h)
description: Verwaltungsclients (z. B. WMI-Anbieter oder Befehlszeilentools) verwenden , um den Status des NAP-Serversystems abzufragen.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- NAP der INapServerInfo-Schnittstelle
- INapServerInfo-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 556c2a5b7e7545038995d5091d46931352f9ee32bddfa31b91237dfa54d69620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626100"
---
# <a name="inapserverinfo-interface"></a>INapServerInfo-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**INapServerInfo** stellt Methoden bereit, die Verwaltungsclients (z. B. WMI-Anbieter oder Befehlszeilentools) verwenden, um den Status des NAP-Serversystems abzufragen.

## <a name="members"></a>Member

Die **INapServerInfo-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerInfo** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapServerInfo-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                   | Beschreibung                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**INapServerInfo::GetFailureCategoryMappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Ruft die Fehlerkategoriezuordnungen für eine angegebene SHV ab.<br/> |
| [**INapServerInfo::GetNapServerInfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Ruft Informationen zum NAP-Server ab.<br/>                  |
| [**INapServerInfo::GetRegisteredSystemHealthValidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Ruft eine Liste registrierter SHVs ab.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Diese Methoden stellen nur statische Informationen zum NAP-Server und seinen Komponenten auf dem System bereit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

