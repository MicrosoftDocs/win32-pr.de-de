---
title: Inapcomponentconfig-Schnittstelle (napcommon. h)
description: Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit.
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Inapcomponentconfig-Schnittstelle NAP
- Inapcomponentconfig-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391778"
---
# <a name="inapcomponentconfig-interface"></a>Inapcomponentconfig-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapcomponentconfig** -Schnittstelle stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit.

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) und [**INapComponentConfig3**](inapcomponentconfig3.md) erben alle Methoden dieser Schnittstelle und sollten stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **inapcomponentconfig** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapcomponentconfig** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapcomponentconfig** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Inapcomponentconfig:: GetConfig**](inapcomponentconfig-getconfig.md)         | Ruft die Konfiguration der SHV-Komponente ab.<br/>                                |
| [**Inapcomponentconfig:: invokeui**](inapcomponentconfig-invokeui.md)           | Hiermit wird die angepasste Benutzeroberfläche für eine SHV-Komponente gestartet.<br/>              |
| [**Inapcomponentconfig:: isuisupported**](inapcomponentconfig-isuisupported.md) | Gibt an, ob die SHV-Komponente eine angepasste Benutzeroberfläche unterstützt.<br/> |
| [**Inapcomponentconfig:: setconfig**](inapcomponentconfig-setconfig.md)         | Legt die Konfiguration der SHV-Komponente fest.<br/>                                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle sollte nicht von Systemintegritäts-Agents (SHAs) oder Quarantäne Erzwingungs Clients (qecs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

