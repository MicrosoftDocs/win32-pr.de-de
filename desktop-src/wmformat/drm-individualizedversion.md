---
title: DRM_IndividualizedVersion
description: Das ATTRIBUT DRM IndividualizedVersion wird im DRM-Header gespeichert und enthält die mindestens erforderliche individualisierte Version für \_ den Zugriff auf den Inhalt.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion des Windows-Medienformats
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d7c9f64a7d4d00e95f8e877e7f33c9e6a8177977eff3b523c25cc1432ac57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704682"
---
# <a name="drm_individualizedversion"></a>DRM \_ IndividualizedVersion

Das **ATTRIBUT DRM \_ IndividualizedVersion** wird im DRM-Header gespeichert und enthält die mindestens erforderliche individualisierte Version für den Zugriff auf den Inhalt.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ IndividualizedVersion

## <a name="data-type"></a>Datentyp

**\_WMT-TYPZEICHENFOLGE \_**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Sie kann [**mitHILFE von IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt und mit [**IWMDRMReader::GetDRMProperty abgerufen werden.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) Dasselbe Dateiattribut kann mit [**DRM \_ DRMHeader \_ IndividualizedVersion abgerufen werden.**](drm-drmheader-individualizedversion.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




