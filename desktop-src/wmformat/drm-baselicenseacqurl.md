---
title: DRM_BaseLicenseAcqURL
description: Das DRM- \_ baselicenseacqurl-Attribut enthält eine partielle Basis-URL, zu der eine Player Anwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128a65eb51d9051243dd439e208207aaf98d5caf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101246"
---
# <a name="drm_baselicenseacqurl"></a>DRM- \_ baselicenabacqurl

Das **DRM- \_ baselicenseacqurl** -Attribut enthält eine partielle Basis-URL, zu der eine Player Anwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ baselicensetup-URL

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dies ist eine optionale Eigenschaft mit Lese-/Schreibzugriff, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)festgelegt und abgerufen wird. Er wird bereitgestellt, damit die Lizenz Verteilungssysteme relative Pfade in den Eigenschaften für die Lizenz Erwerbs-URL verwenden können.

Nachdem Sie diese Eigenschaft festgelegt haben, verfügen alle Teillizenz Erwerbs-URLs in Inhalts Headern über die Basis-URL, die der Vorderseite der partiellen URL hinzugefügt wird, um eine vollständige URL für die Player Anwendung zu bilden. Das Aufrufen von **iwmdrmreader:: getdrmproperty** für **DRM \_ baselicenseacqurl** funktioniert nur in derselben Sitzung, in der es festgelegt wurde. Die-Eigenschaft wird nicht im Content-Header gespeichert. Es ist dynamisch, und nur die relative URL werden im Inhalt gespeichert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




