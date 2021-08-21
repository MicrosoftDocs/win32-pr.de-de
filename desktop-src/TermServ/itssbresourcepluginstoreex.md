---
title: ITsSbResourcePluginStoreEx-Schnittstelle
description: Macht Methoden verfügbar, mit denen Ressourcen-Plug-Ins Objekte wie Sitzungen und Ziele speichern können.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- ITsSbResourcePluginStoreEx-Remotedesktopdienste
- ITsSbResourcePluginStoreEx-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 23c3ba6689f52d592d9c9799b6c7bec0acd58e1afcbc8e7a18e0cb9dbe6db98b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351291"
---
# <a name="itssbresourcepluginstoreex-interface"></a>ITsSbResourcePluginStoreEx-Schnittstelle

Macht Methoden verfügbar, mit denen Ressourcen-Plug-Ins Objekte wie Sitzungen und Ziele speichern können. Diese Methoden fügen diese Objekte hinzu, löschen sie und fragen sie ab.

Diese Schnittstelle ist nur auf Windows Server 2012 R2 mit [installierter KB3091411](https://support.microsoft.com/kb/3091411) verfügbar. Die [**AcquireTargetLock-**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) [**und ReleaseTargetLock-Methoden**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) der [**ITsSbResourcePluginStore-Schnittstelle**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) sind ab Windows Server 2016.

## <a name="members"></a>Member

Die **ITsSbResourcePluginStoreEx-Schnittstelle** erbt von [**ITsSbResourcePluginStore.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) **ITsSbResourcePluginStoreEx** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITsSbResourcePluginStoreEx-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                            | Beschreibung                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Sperrt ein Ziel.<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Fügt dem Ressourcen-Plug-In-Speicher eine Umgebung hinzu.<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Fügt dem Ressourcen-Plug-In-Speicher eine neue Sitzung hinzu.<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Fügt dem Ressourcen-Plug-In-Speicher ein Ziel hinzu.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Löscht ein Ziel.<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Gibt ein Array zurück, das die umgebungen enthält, die im Ressourcen-Plug-In-Speicher vorhanden sind.<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Enumeriert alle landwirtschaftlichen Betriebe, die dem Ressourcen-Plug-In-Speicher hinzugefügt wurden.<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Enumeriert einen angegebenen Satz von Sitzungen.<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Gibt ein Array zurück, das die angegebenen Ziele enthält, die im Ressourcen-Plug-In-Speicher vorhanden sind.<br/> |
| [**GetFarmProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Ruft eine Eigenschaft einer Farm ab.<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Gibt das angegebene Umgebungsobjekt zurück.<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Gibt das Sitzungsobjekt zurück, das über die angegebene Sitzungs-ID verfügt.<br/>                                        |
| [**QueryTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Gibt das Ziel zurück, das über den angegebenen Zielnamen und Farmnamen verfügt.<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Gibt eine Sperre für ein Ziel frei.<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Entfernt die angegebene Umgebung aus dem Ressourcen-Plug-In-Speicher.<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Speichert eine Umgebung.<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Speichert eine Sitzung.<br/>                                                                                     |
| [**SaveTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Speichert ein Ziel.<br/>                                                                                      |
| [**SetEnvironmentProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Legt eine Eigenschaft für eine Umgebung fest.<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Legt eine Eigenschaft für eine Umgebung fest.<br/>                                                                   |
| [**SetSessionState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Legt den Status einer Sitzung fest<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Legt eine Eigenschaft für ein Ziel fest.<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Legt eine Eigenschaft für ein Ziel fest.<br/>                                                                         |
| [**SetTargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Legt den Zustand eines Ziels fest.<br/>                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                             |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Remotedesktop Virtualisierungsschnittstellen](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





