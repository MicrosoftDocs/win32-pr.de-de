---
title: INapComponentConfig3-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3-Schnittstelle NAP
- INapComponentConfig3 Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341360"
---
# <a name="inapcomponentconfig3-interface"></a>INapComponentConfig3-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapComponentConfig3** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapComponentConfig2**](inapcomponentconfig2.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapComponentConfig3** -Schnittstelle erbt von [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentConfig3** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteallconfig**](inapcomponentconfig3-deleteallconfig.md) | Wird von SHVs implementiert und bietet eine Möglichkeit, den SHV-Speicher nach dem Setup in seinen ursprünglichen Zustand zurückzusetzen.<br/>      |
| [**INapComponentConfig3::D eleteconfig**](inapcomponentconfig3-deleteconfig.md)       | Wird von SHVs implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.<br/>  |
| [**INapComponentConfig3:: getconfigfromid**](inapcomponentconfig3-getconfigfromid.md) | Wird von SHVs implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.<br/>  |
| [**INapComponentConfig3:: newconfig**](inapcomponentconfig3-newconfig.md)             | Wird von SHVs implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.<br/>  |
| [**INapComponentConfig3:: setconfigtoid**](inapcomponentconfig3-setconfigtoid.md)     | Wird von SHVs implementiert und bietet eine Möglichkeit, die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





