---
title: Iwmdrmlicentbackuprestorestatus-Schnittstelle
description: Die iwmdrmlicenlbackuprestorestatus-Schnittstelle bietet eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs. Diese Schnittstelle wird mit während der Sicherungs-und Wiederherstellungs Vorgängen generierten Status Ereignissen bereitgestellt.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Iwmdrmlicenabbackuprestorestatus-Schnittstelle Windows Media-Format
- Iwmdrmlicenabbackuprestorestatus-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315993"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>Iwmdrmlicentbackuprestorestatus-Schnittstelle

Die **iwmdrmlicenlbackuprestorestatus** -Schnittstelle bietet eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs.

Diese Schnittstelle wird mit während der Sicherungs-und Wiederherstellungs Vorgängen generierten Status Ereignissen bereitgestellt. Während der Lizenz Sicherung werden mehrere **mewmdrmlicenlbackupprogress** -Ereignisse generiert, von denen jede über eine zugehörige Instanz dieser Schnittstelle verfügt. Das gleiche gilt für **mewmdrmlicenserestoreprogress** -Ereignisse, die während der Wiederherstellung der Lizenz generiert werden.

Wenn Sie einen Zeiger auf eine Instanz der **iwmdrmlicencbackuprestorestatus** -Schnittstelle abrufen möchten, müssen Sie zuerst die **imfmediaevent:: GetValue** -Methode des Progress-Ereignisses aufrufen. Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das die **iwmdrmlicensebackuprestorestatus** -Schnittstelle implementiert.

## <a name="members"></a>Member

Die **iwmdrmlicen* backuprestorestatus** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmlicentarbackuprestorestatus** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmlicentbackuprestorestatus** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Ruft detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang ab.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

