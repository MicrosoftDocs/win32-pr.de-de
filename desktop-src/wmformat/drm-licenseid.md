---
title: DRM_LicenseID
description: Die DRM \_ licenseid-Eigenschaft enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der aktuell geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314345"
---
# <a name="drm_licenseid"></a>DRM- \_ Lizenz seid

Die **DRM \_ licenseid** -Eigenschaft enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der aktuell geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ licenseid

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden.

Die Lizenz-ID wird in einer Lizenz gespeichert, nicht in einer ASF-Datei. Jede einzelne Lizenz verfügt über eine eindeutige ID, die dem Lizenz-Generator zum Zeitpunkt der Erstellung der Lizenz zugewiesen wird. Wenn Sie z. b. zwei Lizenzen für denselben Inhalt erhalten, verfügt jedes über ein anderes licenseid-Attribut. In der Regel müssen Anwendungen diesen Wert nicht abrufen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




