---
title: DRM_DRMHeader_SubscriptionContentID
description: Das DRM \_ DRMHeader \_ SubscriptionContentID-Attribut enthält die Abonnementinhalts-ID.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b273cf95d2bbb271b055eeff3da80a788a38c88bb2e87db37f5a73e6e918e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086150"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>DRM \_ DRMHeader \_ SubscriptionContentID

Das **DRM \_ DRMHeader \_ SubscriptionContentID-Attribut** enthält die Abonnementinhalts-ID.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Die Abonnementinhalts-ID ist optional und wird ausschließlich vom Inhaltsersteller bestimmt. Das Writer-Objekt führt keineRlei Mit diesem Attribut aus. Sie kann mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt und mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




