---
title: INapComponentConfig-Schnittstelle (NapCommon.h)
description: Stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit.
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- INapComponentConfig-Schnittstelle NAP
- INapComponentConfig-Schnittstelle NAP , beschrieben
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
ms.openlocfilehash: 3d0a1c61b3681178089b0cda813155f3629caa233a7995d28cee22b1f65754ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800022"
---
# <a name="inapcomponentconfig-interface"></a>INapComponentConfig-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapComponentConfig-Schnittstelle** stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit.

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) und [**INapComponentConfig3**](inapcomponentconfig3.md) erben alle Methoden dieser Schnittstelle und sollten stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapComponentConfig-Schnittstelle erbt** von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentConfig** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapComponentConfig-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                          | Beschreibung                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)         | Ruft die SHV-Komponentenkonfiguration ab.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Startet die benutzerdefinierte Benutzeroberfläche für eine SHV-Komponente.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Gibt an, ob die SHV-Komponente eine benutzerdefinierte Benutzeroberfläche unterstützt.<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | Legt die SHV-Komponentenkonfiguration fest.<br/>                                     |



 

## <a name="remarks"></a>Hinweise

Diese Schnittstelle sollte nicht von System health agents (SHAs) oder Quarantäneerzwingungsclients (QECs) implementiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

