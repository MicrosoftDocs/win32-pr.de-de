---
title: INapComponentConfig3-Schnittstelle (NapCommon.h)
description: Stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- INapComponentConfig3-Schnittstelle NAP
- INapComponentConfig3-Schnittstelle NAP , beschrieben
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
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803080"
---
# <a name="inapcomponentconfig3-interface"></a>INapComponentConfig3-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapComponentConfig3-Schnittstelle** stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) zum Festlegen und Ändern von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereit.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapComponentConfig2**](inapcomponentconfig2.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapComponentConfig3-Schnittstelle erbt** von [**INapComponentConfig2.**](inapcomponentconfig2.md) **INapComponentConfig3** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentConfig3-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                | Beschreibung                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Wird von SHVs implementiert, um eine Möglichkeit zu bieten, den SHV-Speicher nach dem Setup auf seinen ursprünglichen Zustand zurückzusetzen.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Wird von SHVs implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Wird von SHVs implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen.<br/>  |
| [**INapComponentConfig3::NewConfig**](inapcomponentconfig3-newconfig.md)             | Wird von SHVs implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Wird von SHVs implementiert, um eine Möglichkeit zum Festlegen der Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle sollte nicht von System health agents (SHAs) oder Quarantäneerzwingungsclients (QECs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





