---
title: DRM_IndividualizedVersion
description: Das DRM \_ -Attribut "IndividualizedVersion" wird im DRM-Header gespeichert und enthält die für den Zugriff auf den Inhalt erforderliche minimale individualisierte Version.
ms.assetid: ed3e165c-c6b0-4eea-be79-a715abd4dd0a
keywords:
- DRM_IndividualizedVersion Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ecde48ef3d68e30116cdd7fc8a77179f2282c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314357"
---
# <a name="drm_individualizedversion"></a>DRM- \_ IndividualizedVersion

Das DRM-Attribut " **\_ IndividualizedVersion** " wird im DRM-Header gespeichert und enthält die für den Zugriff auf den Inhalt erforderliche minimale individualisierte Version.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ IndividualizedVersion

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt von DRM Version 7 vorhanden. Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Das gleiche Datei Attribut kann mit [**DRM \_ drmHeader \_ Individual Version**](drm-drmheader-individualizedversion.md)abgerufen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




