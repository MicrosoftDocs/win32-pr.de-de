---
title: DRM_DRMHeader_ContentID
description: Das DRM \_ drmHeader \_ contentid-Attribut enthält die contentid, die vom Inhalts Besitzer generiert wurde.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66edd858451e5d1a58b2a91f9f2362d4cabe9da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948431"
---
# <a name="drm_drmheader_contentid"></a>DRM- \_ drmHeader- \_ contentid

Das **DRM \_ drmHeader \_ contentid** -Attribut enthält die contentid, die vom Inhalts Besitzer generiert wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader \_ contentid

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Zum Festlegen der Inhalts-ID für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) müssen Sie die DRM-Eigenschaft " [**\_ contentid**](drm-contentid.md) " verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




