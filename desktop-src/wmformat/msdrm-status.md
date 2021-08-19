---
title: MSDRM_STATUS-Enumeration (Wmdrmsdk.h)
description: Der MSDRM \_ STATUS-Enumerationstyp definiert Statusbedingungen für das DRM-Subsystem.
ms.assetid: b26600ea-2603-4fca-9408-2d5c88091dcc
keywords:
- MSDRM_STATUS enumeration windows Media Format
- Enumerationsfenster Medienformat
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
ms.openlocfilehash: 0c4c1f9b37f237b1ae2399849ef3100e3d6fdbc12c7ee3bc1d169420e38bb85a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654574"
---
# <a name="msdrm_status-enumeration"></a>MSDRM \_ STATUS-Enumeration

Der **MSDRM \_ STATUS-Enumerationstyp** definiert Statusbedingungen für das DRM-Subsystem.

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

<span id="DRM_ERROR"></span><span id="drm_error"></span>**\_DRM-FEHLER**
</dt> <dd>

Gibt an, dass ein Fehler aufgetreten ist.

</dd> <dt>

<span id="DRM_INFORMATION"></span><span id="drm_information"></span>**\_DRM-INFORMATIONEN**
</dt> <dd>

Gibt an, dass zusätzliche Statusinformationen vorhanden sind.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM \_ BACKUPRESTORE \_ BEGIN**
</dt> <dd>

Gibt an, dass eine Lizenzsicherung oder ein Wiederherstellungsvorgang begonnen wurde.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM \_ BACKUPRESTORE \_ END**
</dt> <dd>

Gibt an, dass ein Lizenzsicherungs- oder Wiederherstellungsvorgang beendet wurde.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM \_ BACKUPRESTORE \_ CONNECTING**
</dt> <dd>

Gibt an, dass eine Lizenzsicherung oder -wiederherstellung ausgeführt wird und dass der Clientcomputer eine Verbindung mit dem Sicherungsserver herstellt.

</dd> <dt>

<span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM \_ BACKUPRESTORE \_ DISCONNECTING**
</dt> <dd>

Gibt an, dass eine Lizenzsicherung oder ein Wiederherstellungsvorgang ausgeführt wird und dass der Clientcomputer die Verbindung mit dem Sicherungsserver trennt.

</dd> <dt>

<span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**\_DRM-FEHLER \_ WITHURL**
</dt> <dd>

Gibt an, dass beim DRM-Vorgang eine ungültige URL aufgetreten ist.

</dd> <dt>

<span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**\_EINGESCHRÄNKTE \_ DRM-LIZENZ**
</dt> <dd>

Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da auf dem Clientcomputer keine Lizenz vorhanden ist, die das erforderliche Recht gewährt.

</dd> <dt>

<span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ ERFORDERT \_ INDIVIDUALISIERUNG**
</dt> <dd>

Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da das DRM-Subsystem individualisiert werden muss.

</dd> <dt>

<span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM \_ PLAY \_ OPL \_ NOTIFICATION**
</dt> <dd>

Gibt an, dass ein Wiedergabevorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabeschutzebene nicht erfüllt wurde.

</dd> <dt>

<span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**\_ \_ DRM-KOPIERVORGANGL-BENACHRICHTIGUNG \_**
</dt> <dd>

Gibt an, dass ein Kopiervorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabeschutzebene nicht erfüllt wurde.

</dd> <dt>

<span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM \_ REFRESHCRL \_ COMPLETE**
</dt> <dd>

Gibt an, dass ein Aufruf von [**IWMDRMSecurity::P erformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) das Aktualisieren einer Sperrliste abgeschlossen hat.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](drm-enumeration-types.md)
</dt> </dl>

 

 





