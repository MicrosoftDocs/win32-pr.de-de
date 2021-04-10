---
title: Itssbresourcepluginstoreex-Schnittstelle
description: Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104295"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Itssbresourcepluginstoreex-Schnittstelle

Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können. Mit diesen Methoden werden diese Objekte hinzugefügt, gelöscht und abgefragt.

Diese Schnittstelle ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar. Die Methoden [**acquiretargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) und [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) der [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) -Schnittstelle sind ab Windows Server 2016 verfügbar.

## <a name="members"></a>Member

Die **itssbresourcepluginstoreex** -Schnittstelle erbt von [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore). **Itssbresourcepluginstoreex** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itssbresourcepluginstoreex** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                            | BESCHREIBUNG                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Acquiretargetlock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Sperrt ein Ziel.<br/>                                                                                      |
| [**Addenvironmentonstore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Fügt dem Ressourcen-Plug-in-Speicher eine Umgebung hinzu.<br/>                                                   |
| [**Addsessionto Store**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Fügt dem Ressourcen-Plug-in-Speicher eine neue Sitzung hinzu.<br/>                                                    |
| [**AddTarget-Store**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Fügt dem Ressourcen-Plug-in-Speicher ein Ziel hinzu.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Löscht ein Ziel.<br/>                                                                                    |
| [**Enumerateenvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Gibt ein Array zurück, das die Umgebungen enthält, die im Ressourcen-Plug-in-Speicher vorhanden sind.<br/>               |
| [**Enumeratefarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Listet alle Farmen auf, die dem Ressourcen-Plug-in-Speicher hinzugefügt wurden.<br/>                         |
| [**Enumeratesessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Listet eine angegebene Gruppe von Sitzungen auf.<br/>                                                              |
| [**Enumeratetargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Gibt ein Array zurück, das die angegebenen Ziele enthält, die im Ressourcen-Plug-in-Speicher vorhanden sind.<br/> |
| [**Getfarmproperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Ruft eine Eigenschaft einer Farm ab.<br/>                                                                      |
| [**Queryenvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Gibt das angegebene Umgebungs Objekt zurück.<br/>                                                            |
| [**Querysessionbysessionid**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Gibt das Sitzungs Objekt zurück, das über die angegebene Sitzungs-ID verfügt.<br/>                                        |
| [**Querytarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Gibt das Ziel mit dem angegebenen Zielnamen und dem Namen der Farm zurück.<br/>                                 |
| [**Releasetargetlock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Gibt eine Sperre für ein Ziel frei.<br/>                                                                         |
| [**Removeumgebfromstore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Entfernt die angegebene Umgebung aus dem Ressourcen-Plug-in-Speicher.<br/>                                   |
| [**Saveenvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Speichert eine Umgebung.<br/>                                                                                |
| [**Savesession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Speichert eine Sitzung.<br/>                                                                                     |
| [**Savetarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Speichert ein Ziel.<br/>                                                                                      |
| [**"Abtenvironmentproperty"**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Legt eine Eigenschaft für eine Umgebung fest.<br/>                                                                   |
| [**"Abtenvironmentpropertywithversioncheck"**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Legt eine Eigenschaft für eine Umgebung fest.<br/>                                                                   |
| [**"Endessionstate"**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Legt den Status einer Sitzung fest<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Legt eine Eigenschaft für ein Ziel fest.<br/>                                                                         |
| [**Settargetpropertywithversioncheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Legt eine Eigenschaft für ein Ziel fest.<br/>                                                                         |
| [**Settargetstate**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Legt den Zustand eines Ziels fest.<br/>                                                                          |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                             |
| Ende des Supports (Server)<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ itssbresourcepluginstoreex ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Remotedesktop Virtualisierungsschnittstellen](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





