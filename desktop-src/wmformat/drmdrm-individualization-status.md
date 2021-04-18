---
title: DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)
description: Der DRM- \_ Individualisierungs \_ Status-Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung. | DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS-Enumeration Windows Media-Format
- Enumeration Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361443"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="0e0e6-106">DRM_INDIVIDUALIZATION_STATUS-Enumeration (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="0e0e6-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="0e0e6-107">Der **DRM- \_ Individualisierungs \_ Status** -Enumerationstyp definiert die gültigen Zustände für die DRM-Individualisierung.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0e6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e0e6-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="0e0e6-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0e0e6-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0e0e6-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**Indi nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-111">Dieser Wert ist für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Indi \_ Begin**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-113">Gibt den Beginn des Individualisierungs Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**Indi \_ erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-115">Gibt an, dass der Individualisierungsprozess abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**Indi \_ Fail**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-117">Gibt an, dass der Individualisierungsprozess fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**Indi \_ Abbrechen**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-119">Gibt an, dass der Individualisierungsprozess von der Anwendung abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**Indi \_ herunterladen**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-121">Gibt an, dass das Sicherheits Upgrade heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="0e0e6-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**Indi- \_ Installation**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="0e0e6-123">Gibt an, dass das Sicherheits Upgrade installiert wird.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e0e6-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e0e6-124">Remarks</span></span>

<span data-ttu-id="0e0e6-125">Diese Enumeration wird von der [**WM \_ Individual \_ Status**](drmwm-individualize-status.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e0e6-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0e6-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e0e6-126">Requirements</span></span>



| <span data-ttu-id="0e0e6-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e0e6-127">Requirement</span></span> | <span data-ttu-id="0e0e6-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0e0e6-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0e6-129">Header</span><span class="sxs-lookup"><span data-stu-id="0e0e6-129">Header</span></span><br/> | <dl> <span data-ttu-id="0e0e6-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e0e6-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e0e6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e0e6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0e6-132">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="0e0e6-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





