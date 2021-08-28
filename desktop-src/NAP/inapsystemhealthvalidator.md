---
title: INapSystemHealthValidator-Schnittstelle (NapSystemHealthValidator.h)
description: Muss von SHV-Entwicklern implementiert werden, damit das NAP-System mit einer SHV kommunizieren kann.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- INapSystemHealthValidator-Schnittstelle NAP
- INapSystemHealthValidator-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7310afe1c61dd61344bd1ed355f78735dc7785f9016bbcbb702073b2a06feba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686060"
---
# <a name="inapsystemhealthvalidator-interface"></a>INapSystemHealthValidator-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der **INapSystemHealthValidator** stellt Methoden bereit, die von SHV-Entwicklern implementiert werden müssen, damit das NAP-System mit einer SHV kommunizieren kann.

## <a name="members"></a>Member

Die **INapSystemHealthValidator-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidator** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthValidator-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator::Validate**](inapsystemhealthvalidator-validate-method.md) | Das NAP-System ruft diese anwendungsdefinierte Methode auf, um die von einem Client empfangene [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu überprüfen. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

