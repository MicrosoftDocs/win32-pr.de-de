---
title: MSDRM_STATUS-Enumeration (wmdrmsdk. h)
description: Der \_ Enumerationstyp "msdrm-Status" definiert Status Bedingungen für das DRM-Subsystem.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- MSDRM_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2a73de9e33216e22a01966be8f2ed6a3185fdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368374"
---
# <a name="msdrm_status-enumeration"></a>Msdrm- \_ statusenumeration

Der Enumerationstyp " **msdrm- \_ Status** " definiert Status Bedingungen für das DRM-Subsystem.

## <a name="syntax"></a>Syntax


```C++
typedef enum MSDRM_STATUS { 
  DRM_ERROR                        = 0,
  DRM_INFORMATION                  = 1,
  DRM_BACKUPRESTORE_BEGIN          = 2,
  DRM_BACKUPRESTORE_END            = 3,
  DRM_BACKUPRESTORE_CONNECTING     = 4,
  DRM_BACKUPRESTORE_DISCONNECTING  = 5,
  DRM_ERROR_WITHURL                = 6,
  DRM_RESTRICTED_LICENSE           = 7,
  DRM_NEEDS_INDIVIDUALIZATION      = 8,
  DRM_PLAY_OPL_NOTIFICATION        = 9,
  DRM_COPY_OPL_NOTIFICATION        = 10,
  DRM_REFRESHCRL_COMPLETE          = 11
} ;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM- \_ Fehler**
</dt> <dd>

Gibt an, dass ein Fehler aufgetreten ist.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM- \_ Informationen**
</dt> <dd>

Gibt an, dass zusätzliche Statusinformationen vorhanden sind.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM- \_ backuprestore- \_ Anfang**
</dt> <dd>

Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang begonnen hat.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM- \_ backuprestore- \_ Ende**
</dt> <dd>

Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang beendet wurde.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM- \_ backuprestore-Verbindung wird hergestellt \_**
</dt> <dd>

Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang ausgeführt wird und dass der Client Computer eine Verbindung mit dem Sicherungs Server herstellt.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM- \_ backuprestore wird \_ getrennt**
</dt> <dd>

Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang ausgeführt wird und dass der Client Computer die Verbindung mit dem Sicherungs Server trennt.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM- \_ Fehler \_ withurl**
</dt> <dd>

Gibt an, dass der DRM-Vorgang eine ungültige URL gefunden hat.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**eingeschränkte DRM- \_ \_ Lizenz**
</dt> <dd>

Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da auf dem Client Computer keine Lizenz vorhanden ist, die das erforderliche Recht

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ erfordert \_ Individualisierung**
</dt> <dd>

Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da das DRM-Subsystem individuell sein muss.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM- \_ Wiedergabe- \_ OPL- \_ Benachrichtigung**
</dt> <dd>

Gibt an, dass ein Wiedergabe Vorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabe Schutz Ebene nicht erfüllt wurde.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM- \_ Kopier- \_ OPL- \_ Benachrichtigung**
</dt> <dd>

Gibt an, dass ein Kopiervorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabe Schutz Ebene nicht erfüllt wurde.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_vollständige DRM-CRL \_**
</dt> <dd>

Gibt an, dass ein [**callmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Befehl die Aktualisierung einer Sperr Liste abgeschlossen hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





