---
title: INapClientManagement2-Schnittstelle (NapManagement.h)
description: Stellt Methoden für die NAP-Clientverwaltung zur | INapClientManagement2-Schnittstelle (NapManagement.h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- INapClientManagement2-Schnittstelle NAP
- INapClientManagement2-Schnittstelle NAP , beschrieben
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
ms.openlocfilehash: 4f459e6fa0d883203bf52ebbd0aaab06ee93cef00d1fb52af3d670f71cf7ab52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800100"
---
# <a name="inapclientmanagement2-interface"></a>INapClientManagement2-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapClientManagement2-Schnittstelle** stellt Methoden für die NAP-Clientverwaltung bereit.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapClientManagement**](inapclientmanagement.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapClientManagement2-Schnittstelle** erbt von [**INapClientManagement**](inapclientmanagement.md). **INapClientManagement2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapClientManagement2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                    | Beschreibung                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Ruft Informationen über den Isolationsstatus und den erweiterten Isolationsstatus des Nap-Clients ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





