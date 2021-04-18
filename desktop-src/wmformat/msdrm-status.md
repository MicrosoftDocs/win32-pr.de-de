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
# <a name="msdrm_status-enumeration"></a><span data-ttu-id="1cf0b-105">Msdrm- \_ statusenumeration</span><span class="sxs-lookup"><span data-stu-id="1cf0b-105">MSDRM\_STATUS enumeration</span></span>

<span data-ttu-id="1cf0b-106">Der Enumerationstyp " **msdrm- \_ Status** " definiert Status Bedingungen für das DRM-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-106">The **MSDRM\_STATUS** enumeration type defines status conditions for the DRM subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf0b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cf0b-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="1cf0b-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1cf0b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1cf0b-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-109"><span id="DRM_ERROR"></span><span id="drm_error"></span>**DRM\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-110">Gibt an, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-110">Specifies that an error has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-111"><span id="DRM_INFORMATION"></span><span id="drm_information"></span>**DRM\_INFORMATION**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-112">Gibt an, dass zusätzliche Statusinformationen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-112">Specifies that there is additional status information.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM- \_ backuprestore- \_ Anfang**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-113"><span id="DRM_BACKUPRESTORE_BEGIN"></span><span id="drm_backuprestore_begin"></span>**DRM\_BACKUPRESTORE\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-114">Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-114">Specifies that a license backup or restore operation has begun.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM- \_ backuprestore- \_ Ende**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-115"><span id="DRM_BACKUPRESTORE_END"></span><span id="drm_backuprestore_end"></span>**DRM\_BACKUPRESTORE\_END**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-116">Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-116">Specifies that a license backup or restore operation has ended.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM- \_ backuprestore-Verbindung wird hergestellt \_**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-117"><span id="DRM_BACKUPRESTORE_CONNECTING"></span><span id="drm_backuprestore_connecting"></span>**DRM\_BACKUPRESTORE\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-118">Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang ausgeführt wird und dass der Client Computer eine Verbindung mit dem Sicherungs Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-118">Specifies that a license backup or restore operation is in progress and that the client computer is connecting with the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM- \_ backuprestore wird \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-119"><span id="DRM_BACKUPRESTORE_DISCONNECTING"></span><span id="drm_backuprestore_disconnecting"></span>**DRM\_BACKUPRESTORE\_DISCONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-120">Gibt an, dass eine Lizenz Sicherung oder ein Wiederherstellungs Vorgang ausgeführt wird und dass der Client Computer die Verbindung mit dem Sicherungs Server trennt.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-120">Specifies that a license backup or restore operation is in progress and that the client computer is disconnecting from the backup server.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM- \_ Fehler \_ withurl**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-121"><span id="DRM_ERROR_WITHURL"></span><span id="drm_error_withurl"></span>**DRM\_ERROR\_WITHURL**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-122">Gibt an, dass der DRM-Vorgang eine ungültige URL gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-122">Specifies that the DRM operation has encountered a bad URL.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**eingeschränkte DRM- \_ \_ Lizenz**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-123"><span id="DRM_RESTRICTED_LICENSE"></span><span id="drm_restricted_license"></span>**DRM\_RESTRICTED\_LICENSE**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-124">Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da auf dem Client Computer keine Lizenz vorhanden ist, die das erforderliche Recht</span><span class="sxs-lookup"><span data-stu-id="1cf0b-124">Specifies that the DRM operation cannot continue because no license granting the required right exists on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM \_ erfordert \_ Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-125"><span id="DRM_NEEDS_INDIVIDUALIZATION"></span><span id="drm_needs_individualization"></span>**DRM\_NEEDS\_INDIVIDUALIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-126">Gibt an, dass der DRM-Vorgang nicht fortgesetzt werden kann, da das DRM-Subsystem individuell sein muss.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-126">Specifies that the DRM operation cannot continue because the DRM subsystem needs to be individualized.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM- \_ Wiedergabe- \_ OPL- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-127"><span id="DRM_PLAY_OPL_NOTIFICATION"></span><span id="drm_play_opl_notification"></span>**DRM\_PLAY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-128">Gibt an, dass ein Wiedergabe Vorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabe Schutz Ebene nicht erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-128">Specifies that a playback operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM- \_ Kopier- \_ OPL- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-129"><span id="DRM_COPY_OPL_NOTIFICATION"></span><span id="drm_copy_opl_notification"></span>**DRM\_COPY\_OPL\_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-130">Gibt an, dass ein Kopiervorgang nicht abgeschlossen werden kann, da eine Anforderung der Ausgabe Schutz Ebene nicht erfüllt wurde.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-130">Specifies that a copy operation cannot be completed because an output protection level requirement has not been met.</span></span>

</dd> <dt>

<span data-ttu-id="1cf0b-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**\_vollständige DRM-CRL \_**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-131"><span id="DRM_REFRESHCRL_COMPLETE"></span><span id="drm_refreshcrl_complete"></span>**DRM\_REFRESHCRL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="1cf0b-132">Gibt an, dass ein [**callmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Befehl die Aktualisierung einer Sperr Liste abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-132">Specifies that a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) has completed refreshing a revocation list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cf0b-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cf0b-133">Remarks</span></span>

<span data-ttu-id="1cf0b-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="1cf0b-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cf0b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cf0b-135">Requirements</span></span>



| <span data-ttu-id="1cf0b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cf0b-136">Requirement</span></span> | <span data-ttu-id="1cf0b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1cf0b-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf0b-138">Header</span><span class="sxs-lookup"><span data-stu-id="1cf0b-138">Header</span></span><br/> | <dl> <span data-ttu-id="1cf0b-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf0b-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf0b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cf0b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf0b-141">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="1cf0b-141">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





