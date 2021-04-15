---
title: Use_DRM
description: Das use \_ DRM-Attribut weist das Writer-Objekt an, DRM-Version 1-Schutz auf die aktuelle Datei anzuwenden.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Use_DRM Windows Media-Format
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516592"
---
# <a name="use_drm"></a>Verwenden von \_ DRM

Das **use \_ DRM** -Attribut weist das Writer-Objekt an, DRM-Version 1-Schutz auf die aktuelle Datei anzuwenden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmuse \_ DRM

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , um diese Eigenschaft beim Erstellen von DRM-Version 1-Inhalt auf **true** festzulegen. Auf diese Eigenschaft kann nicht über das Reader-Objekt zugegriffen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




