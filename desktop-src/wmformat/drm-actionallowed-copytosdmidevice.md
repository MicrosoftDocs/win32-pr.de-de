---
title: DRM_ActionAllowed_CopyToSDMIDevice
description: Das ATTRIBUT DRM \_ ActionAllowed \_ CopyToSDMIDevice gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.
ms.assetid: 3ffb9c8f-5640-4ab5-9939-f9525ab960c6
keywords:
- DRM_ActionAllowed_CopyToSDMIDevice Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CopyToSDMIDevice
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a868eab52d354672802ef1f736bbc2754af605371708247415cbe78a42442e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809420"
---
# <a name="drm_actionallowed_copytosdmidevice"></a>DRM \_ ActionAllowed \_ CopyToSDMIDevice

Das **ATTRIBUT DRM \_ ActionAllowed \_ CopyToSDMIDevice** gibt an, ob der Inhalt auf ein SDMI-Gerät kopiert werden darf.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Windows Medien-DRM 10-Lizenzen verwenden die Kopieraktion, um das Kopieren auf Geräte einzuschränken. Überprüfen Sie die [**EIGENSCHAFT DRM \_ ActionAllowed \_ Copy,**](drm-actionallowed-copy.md) um zu ermitteln, ob das Kopieren zulässig ist.

Dies ist eine schreibgeschützte Eigenschaft, die mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




