---
title: DRM_DRMHeader_ContentDistributor
description: Das Attribut "DRM \_ drmHeader \_ contentdistributor" enthält eine Zeichenfolge, die den Inhalts Verteiler Bezeichner.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2494f80e612e03f9d25372d38e875c1df814fd7d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106342112"
---
# <a name="drm_drmheader_contentdistributor"></a>DRM- \_ drmHeader- \_ contentdistributor

Das Attribut " **DRM \_ drmHeader \_ contentdistributor** " enthält eine Zeichenfolge, die den Inhalts Verteiler Bezeichner.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader- \_ contentdistributor

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Die Inhalts-ID ist optional und wird nur vom Ersteller des Inhalts bestimmt. Das Writer-Objekt hat nichts mit diesem Attribut. Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




