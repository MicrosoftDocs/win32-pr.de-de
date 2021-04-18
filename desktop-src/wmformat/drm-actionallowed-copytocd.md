---
title: DRM_ActionAllowed_CopyToCD
description: Das vom DRM-Attribut ausführbare \_ \_ Attribut copyper CD gibt an, ob der Inhalt auf eine CD kopiert werden darf.
ms.assetid: c650bb2e-6cec-404a-8ece-7a5687cda99f
keywords:
- DRM_ActionAllowed_CopyToCD Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToCD
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba214fb2f067ba523222f92211bf7a9412a1634
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340684"
---
# <a name="drm_actionallowed_copytocd"></a>DRM- \_ Aktions zulässige \_ CopyTo-CD

Das vom DRM-Attribut ausführbare Attribut **\_ \_ copyper CD** gibt an, ob der Inhalt auf eine CD kopiert werden darf.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Aktions zulässige \_ copyper-CD

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Windows Media DRM 10-Lizenzen verwenden Sie die Kopier Aktion, um das Kopieren auf CD einzuschränken. Überprüfen Sie die Eigenschaft " [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md) ", um zu bestimmen, ob das Kopieren zulässig ist.

Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




