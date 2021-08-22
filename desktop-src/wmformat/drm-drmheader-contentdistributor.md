---
title: DRM_DRMHeader_ContentDistributor
description: Das DRM \_ DRMHeader \_ ContentDistributor-Attribut enthält eine Zeichenfolge, die den Inhaltsverteiler identifiziert.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- DRM_DRMHeader_ContentDistributor Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586460"
---
# <a name="drm_drmheader_contentdistributor"></a>DRM \_ DRMHeader \_ ContentDistributor

Das **DRM \_ DRMHeader \_ ContentDistributor-Attribut** enthält eine Zeichenfolge, die den Inhaltsverteiler identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Die Inhalts-ID ist optional und wird ausschließlich vom Inhaltsersteller bestimmt. Das Writer-Objekt führt keineRlei Mit diesem Attribut aus. Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Sie kann mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt und mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




