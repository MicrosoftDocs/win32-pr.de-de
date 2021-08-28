---
title: DRM_IsDRMCached
description: Die DRM \_ IsDRMCached-Eigenschaft gibt an, ob DRM-Lizenzinformationen der Version 1 auf dem lokalen Computer gespeichert wurden.
ms.assetid: 868e3ada-d608-41d6-93d7-0b7930cbf2f9
keywords:
- DRM_IsDRMCached Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_IsDRMCached
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9b5bbcf7e4e1c11c8ae992156b7541ac66c7a9d43f2cb1d52878d1ee6762d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709040"
---
# <a name="drm_isdrmcached"></a>DRM \_ IsDRMCached

Die **DRM \_ IsDRMCached-Eigenschaft** gibt an, ob DRM-Lizenzinformationen der Version 1 auf dem lokalen Computer gespeichert wurden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ IsDRMCached

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist eine schreibgeschützte Eigenschaft, die mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird. Dies ist **TRUE,** wenn die Lizenzerwerbs-URL mit einer von zwei urls übereinstimmt, die für den lokalen Lizenzerwerb in DRM Version 1 verwendet werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




