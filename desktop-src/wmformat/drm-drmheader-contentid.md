---
title: DRM_DRMHeader_ContentID
description: Das DRM \_ DRMHeader \_ ContentID-Attribut enthält die contentID, die vom Inhaltsbesitzer generiert wurde.
ms.assetid: fda38778-2fdf-4218-aad2-e4cf351d74e9
keywords:
- DRM_DRMHeader_ContentID Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b17df75902ec41eed935a9b10dbbf4799c92bae2a54c76b4ed676c9e7a3a572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586428"
---
# <a name="drm_drmheader_contentid"></a>DRM \_ DRMHeader \_ ContentID

Das **DRM \_ DRMHeader \_ ContentID-Attribut** enthält die contentID, die vom Inhaltsbesitzer generiert wurde.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ DRMHeader \_ ContentID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Sie kann mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen werden. Um die Inhalts-ID für die Datei mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festzulegen, müssen Sie die [**DRM \_ ContentID-Eigenschaft**](drm-contentid.md) verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




