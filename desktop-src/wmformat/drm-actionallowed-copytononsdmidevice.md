---
title: DRM_ActionAllowed_CopyToNonSDMIDevice
description: Das vom DRM- \_ \_ Attribut ausführbare copytononsdmidevice-Attribut gibt an, ob der Inhalt auf ein nicht-SDMI-Gerät kopiert werden darf.
ms.assetid: 517ceeb5-4979-4667-ba54-8b9b1c6069f2
keywords:
- DRM_ActionAllowed_CopyToNonSDMIDevice Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToNonSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8043c6384fbe0ce57ba56fc9799810d7b6a126b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038584"
---
# <a name="drm_actionallowed_copytononsdmidevice"></a>DRM-Aktions zulässiges \_ \_ copytononsdmidevice

Das vom DRM-Attribut ausführbare **\_ \_ copytononsdmidevice** -Attribut gibt an, ob der Inhalt auf ein nicht-SDMI-Gerät kopiert werden darf.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Aktions zulässige \_ copytononsdmidevice

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Windows Media DRM 10-Lizenzen verwenden Sie die Kopier Aktion, um das Kopieren auf Geräte einzuschränken. Überprüfen Sie die Eigenschaft " [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md) ", um zu bestimmen, ob das Kopieren zulässig ist.

Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




