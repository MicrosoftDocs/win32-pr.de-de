---
title: Inapserverinfo-Schnittstelle (napservermanagement. h)
description: Verwaltungs Clients (z. b. WMI-Anbieter oder Befehlszeilen Tools) verwenden, um den Status des NAP-Server Systems abzufragen.
ms.assetid: 3c6d3f76-ea63-4cb2-bac7-e5668e50b7a7
keywords:
- Inapserverinfo-Schnittstelle NAP
- Inapserverinfo-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: ec17e3303fe4af4d359279de6c5fa7aa5f34d409
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339161"
---
# <a name="inapserverinfo-interface"></a>Inapserverinfo-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**Inapserverinfo** stellt Methoden bereit, mit denen Verwaltungs Clients (z. b. WMI-Anbieter oder Befehlszeilen Tools) den Status des NAP-Server Systems Abfragen.

## <a name="members"></a>Member

Die **inapserverinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapserverinfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapserverinfo** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                   | BESCHREIBUNG                                                             |
|:-------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**Inapserverinfo:: getfailurecategorymappings**](inapserverinfo-getfailurecategorymappings-method.md)                   | Ruft die Zuordnungen der Fehlerkategorien für einen angegebenen SHV ab.<br/> |
| [**Inapserverinfo:: getnapserverinfo**](inapserverinfo-getnapserverinfo-method.md)                                       | Ruft Informationen zum NAP-Server ab.<br/>                  |
| [**Inapserverinfo:: getregisteredsystemhealthvalidators**](inapserverinfo-getregisteredsystemhealthvalidators-method.md) | Ruft eine Liste registrierter SHVs ab.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Methoden bieten nur statische Informationen über den NAP-Server und dessen Komponenten im System.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napservermanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napservermanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

