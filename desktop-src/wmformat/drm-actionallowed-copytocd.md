---
title: DRM_ActionAllowed_CopyToCD
description: Das DRM \_ ActionAllowed CopyToCD-Attribut gibt an, ob der Inhalt auf eine \_ CD kopiert werden darf.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852d44a4c812aed0d2f188b5ab18e9b74a1813bd9605bf348ca23b96b72f7d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809410"
---
# <a name="drm_actionallowed_copytocd"></a>DRM \_ ActionAllowed \_ CopyToCD

Das **DRM \_ ActionAllowed \_ CopyToCD-Attribut** gibt an, ob der Inhalt auf eine CD kopiert werden darf.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Windows Media DRM 10-Lizenzen verwenden die Kopieraktion, um das Kopieren auf CD einzuschränken. Überprüfen Sie die [**EIGENSCHAFT DRM \_ ActionAllowed \_ Copy**](drm-actionallowed-copy.md) , um zu bestimmen, ob das Kopieren zulässig ist.

Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**IWMDRMReader::GetDRMProperty abgerufen wird.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




