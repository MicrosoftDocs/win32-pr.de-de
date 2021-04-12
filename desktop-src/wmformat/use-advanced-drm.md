---
title: Use_Advanced_DRM
description: Das use \_ Advanced \_ DRM-Attribut gibt an, ob DRM-Version 7 verwendet wird, um den Inhalt zu schützen.
ms.assetid: a385152f-d72e-473c-93a0-5697659df23c
keywords:
- Use_Advanced_DRM Windows Media-Format
topic_type:
- apiref
api_name:
- Use_Advanced_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8720d5b401a1a1cec5240920bfb4a3811012420
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104208722"
---
# <a name="use_advanced_drm"></a>Verwenden von \_ Advanced \_ DRM

Das **use \_ Advanced \_ DRM** -Attribut gibt an, ob DRM-Version 7 verwendet wird, um den Inhalt zu schützen.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmuse \_ Advanced \_ DRM

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ bool**

## <a name="remarks"></a>Bemerkungen

Dabei handelt es sich um eine Eigenschaft mit Lese-/Schreibzugriff, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) abgerufen und mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt wird. Auf diese Eigenschaft kann nicht über das Reader-Objekt zugegriffen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




