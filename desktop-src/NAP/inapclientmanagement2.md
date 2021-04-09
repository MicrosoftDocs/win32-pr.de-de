---
title: INapClientManagement2-Schnittstelle (napmanagement. h)
description: Stellt Methoden für die NAP-Client Verwaltung bereit. | INapClientManagement2-Schnittstelle (napmanagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2-Schnittstelle NAP
- INapClientManagement2 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050808"
---
# <a name="inapclientmanagement2-interface"></a>INapClientManagement2-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapClientManagement2** -Schnittstelle bietet Methoden für die NAP-Client Verwaltung.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**inapclientmanagement**](inapclientmanagement.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapClientManagement2** -Schnittstelle erbt von [**inapclientmanagement**](inapclientmanagement.md). **INapClientManagement2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapClientManagement2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                    | BESCHREIBUNG                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2:: getsystemisolationinfoex**](inapclientmanagement2-getsystemisolationinfoex.md) | Ruft Informationen zum Isolations Status und zum erweiterten Isolations Status des NAP-Clients ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Napmanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napmanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapclientmanagement**](inapclientmanagement.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





