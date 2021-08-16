---
title: DRM_DRMHeader_IndividualizedVersion
description: Das \_ DRM DRMHeaderIndividualizedVersion-Attribut enthält die minimale individualisierte Version, die zum Wiedergeben der Datei erforderlich ist.
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793fa81a7c6c57542991d582607edb0cf3e38b62b037ad46974a4211a7ef8ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931180"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ DRMHeader \_ IndividualizedVersion

Das **\_ DRM DRMHeaderIndividualizedVersion-Attribut** enthält die minimale individualisierte Version, die zum Wiedergeben der Datei erforderlich ist.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Sie kann mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen werden. Um die individualisierte Version (auch als Sicherheitsversion bezeichnet) für die Datei mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festzulegen, müssen Sie die [**\_ DRM-Eigenschaft IndividualizedVersion**](drm-individualizedversion.md) verwenden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




