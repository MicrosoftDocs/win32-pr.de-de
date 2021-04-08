---
title: DRM_DRMHeader_LicenseAcqURL
description: Das \_ Attribut DRM drmHeader \_ licen* AcqURL enthält die Lizenz Erwerbs-URL für eine DRM-Lizenz der Version 7.
ms.assetid: 00c788b4-b291-4df5-9926-0badc7357faf
keywords:
- DRM_DRMHeader_LicenseAcqURL Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_LicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c394df01703befbb17c61b340b8ea4239740ac3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038552"
---
# <a name="drm_drmheader_licenseacqurl"></a>DRM \_ drmHeader \_ licenanacqurl

Das Attribut **DRM \_ drmHeader \_ licen* AcqURL** enthält die Lizenz Erwerbs-URL für eine DRM-Lizenz der Version 7.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader \_ licengacqurl

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Wenn Sie die Lizenz Erwerbs-URL für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festlegen möchten, müssen Sie die Eigenschaft [**DRM \_ licenseacqurl**](drm-licenseacqurl.md) verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




