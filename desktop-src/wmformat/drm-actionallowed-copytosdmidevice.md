---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: Das vom DRM-Attribut ausführbare \_ \_ copytosdmidevice-Attribut gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f61da53fd060bd4fb06dbbb7586d923ac17fc0f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389823"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>DRM-Aktions zulässiges \_ \_ copytosdmidevice

Das vom DRM-Attribut ausführbare **\_ \_ copytosdmidevice** -Attribut gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Aktions zulässige \_ copytosdmidevice

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Windows Media DRM 10-Lizenzen verwenden Sie die Kopier Aktion, um das Kopieren auf Geräte einzuschränken. Überprüfen Sie die Eigenschaft " [**DRM- \_ Aktions zulässige \_ Kopie**](drm-actionallowed-copy.md) ", um zu bestimmen, ob das Kopieren zulässig ist.

Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




