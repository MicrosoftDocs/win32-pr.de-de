---
title: IWMDRMLicenseBackupRestoreStatus-Schnittstelle
description: Die IWMDRMLicenseBackupRestoreStatus-Schnittstelle stellt eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenzsicherung oder einem Wiederherstellungsvorgang bereit. Diese Schnittstelle wird mit Statusereignissen bereitgestellt, die während lizenzsicherungs- und wiederherstellungsvorgängen generiert werden.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- IWMDRMLicenseBackupRestoreStatus-Schnittstelle windows Medienformat
- IWMDRMLicenseBackupRestoreStatus-Schnittstelle windows Media Format , beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26583a2911545cd256598025806d238c2f98f84434b4f23d9f13f952bfd15927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847039"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>IWMDRMLicenseBackupRestoreStatus-Schnittstelle

Die **IWMDRMLicenseBackupRestoreStatus-Schnittstelle** stellt eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenzsicherung oder einem Wiederherstellungsvorgang bereit.

Diese Schnittstelle wird mit Statusereignissen bereitgestellt, die während lizenzsicherungs- und wiederherstellungsvorgängen generiert werden. Während der Lizenzsicherung werden mehrere **MEWMDRMLicenseBackupProgress-Ereignisse** generiert, von denen jedes über eine zugehörige Instanz dieser Schnittstelle verfügt. Dasselbe gilt für **MEWMDRMLicenseRestoreProgress-Ereignisse,** die während der Lizenzwiederherstellung generiert werden.

Um einen Zeiger auf eine Instanz der **IWMDRMLicenseBackupRestoreStatus-Schnittstelle** abzurufen, müssen Sie zunächst die **METHODE "POINTERMediaEvent::GetValue"** des Statusereignisses aufrufen. Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown-Schnittstelle** des Objekts, das die **IWMDRMLicenseBackupRestoreStatus-Schnittstelle** implementiert.

## <a name="members"></a>Member

Die **IWMDRMLicenseBackupRestoreStatus-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMLicenseBackupRestoreStatus** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMDRMLicenseBackupRestoreStatus-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Ruft detaillierte Statusinformationen zu einer Lizenzsicherung oder einem Wiederherstellungsvorgang ab.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

