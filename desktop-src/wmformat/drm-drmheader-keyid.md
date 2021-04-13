---
title: DRM_DRMHeader_KeyID
description: Das Attribut "DRM \_ drmHeader \_ keyid" enthält die Schlüssel-ID für die Datei.
ms.assetid: cf9fe829-8473-4dd5-9a99-48b709fec0d8
keywords:
- DRM_DRMHeader_KeyID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_DRMHeader_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebbf2f548725309717993bf29e48de2bf78ed17
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314285"
---
# <a name="drm_drmheader_keyid"></a>DRM- \_ drmHeader- \_ keyid

Das Attribut " **DRM \_ drmHeader \_ keyid** " enthält die Schlüssel-ID für die Datei.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ drmHeader- \_ keyid

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Wenn Sie die Schlüssel-ID für die Datei mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festlegen möchten, müssen Sie die [**DRM- \_ keyid**](drm-keyid.md) -Eigenschaft verwenden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




