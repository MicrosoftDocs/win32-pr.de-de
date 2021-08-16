---
title: Use_DRM
description: Das Use \_ DRM-Attribut weist das Writer-Objekt an, schutz von DRM Version 1 auf die aktuelle Datei anzuwenden.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM Windows-Medienformat
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845301"
---
# <a name="use_drm"></a>Verwenden \_ von DRM

Das **Use \_ DRM-Attribut** weist das Writer-Objekt an, schutz von DRM Version 1 auf die aktuelle Datei anzuwenden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BOOL**

## <a name="remarks"></a>Hinweise

Verwenden [**Sie IWMHeaderInfo::SetAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) um diese Eigenschaft beim Erstellen von DRM-Inhalt der Version 1 auf **TRUE** zu setzen. Auf diese Eigenschaft kann nicht über das Readerobjekt zugegriffen werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




