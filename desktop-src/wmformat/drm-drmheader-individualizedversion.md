---
title: DRM_DRMHeader_IndividualizedVersion
description: Das DRM- \_ Attribut "drmheaderindividualizedversion" enthält die mindestens erforderliche individualisierte Version, die für die Wiedergabe der Datei erforderlich ist.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338438"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ drmHeader \_ IndividualizedVersion

Das DRM-Attribut " **\_ drmheaderindividualizedversion** " enthält die mindestens erforderliche individualisierte Version, die für die Wiedergabe der Datei erforderlich ist.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader \_ IndividualizedVersion

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Zum Festlegen der individualisierten Version (auch als Sicherheitsversion bezeichnet) für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) müssen Sie die [**DRM \_ Individual Version**](drm-individualizedversion.md) -Eigenschaft verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




