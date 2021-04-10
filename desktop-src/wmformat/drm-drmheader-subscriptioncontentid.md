---
title: DRM_DRMHeader_SubscriptionContentID
description: Das \_ Attribut DRM drmHeader \_ abonnementcontentid enthält die Abonnement Inhalts-ID.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- DRM_DRMHeader_SubscriptionContentID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948430"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>DRM- \_ drmHeader- \_ abonnemencontentid

Das Attribut **DRM \_ drmHeader \_ abonnementcontentid** enthält die Abonnement Inhalts-ID.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader \_ abonnemencontentid

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Die Abonnement Inhalts-ID ist optional und wird nur vom Ersteller des Inhalts bestimmt. Das Writer-Objekt hat nichts mit diesem Attribut. Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




