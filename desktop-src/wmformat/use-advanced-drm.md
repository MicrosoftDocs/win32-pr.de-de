---
title: Use_Advanced_DRM
description: Das \_ Use Advanced \_ DRM-Attribut gibt an, ob DRM Version 7 zum Schützen des Inhalts verwendet wird.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM Windows-Medienformat
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a11731fbe212c8b87cd52300da1885206230c7329491a6512ab3c261923c74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658220"
---
# <a name="use_advanced_drm"></a>Verwenden von \_ Advanced \_ DRM

Das Use **\_ Advanced \_ DRM-Attribut** gibt an, ob DRM Version 7 zum Schützen des Inhalts verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMUse \_ Advanced \_ DRM

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Dies ist eine Lese-/Schreibeigenschaft, die mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) abgerufen und mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt wird. Auf diese Eigenschaft kann nicht über das Readerobjekt zugegriffen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




