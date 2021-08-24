---
title: DRM_BaseLicenseAcqURL
description: Das DRM \_ BaseLicenseAcqURL-Attribut enthält eine partielle Basis-URL, zu der eine Playeranwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- DRM_BaseLicenseAcqURL Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77827068ee8a491cd732b28e5b8d60e1868ec66c04c72156f08358dd7d3751d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659000"
---
# <a name="drm_baselicenseacqurl"></a>DRM \_ BaseLicenseAcqURL

Das **DRM \_ BaseLicenseAcqURL-Attribut** enthält eine partielle Basis-URL, zu der eine Playeranwendung navigieren muss, um eine Lizenz für den Inhalt zu erhalten.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dies ist eine optionale Lese-/Schreibeigenschaft, die mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)festgelegt und abgerufen wird. Sie wird bereitgestellt, damit Lizenzverteilungssysteme relative Pfade in den Eigenschaften der Lizenzerwerbs-URL verwenden können.

Nach dem Festlegen dieser Eigenschaft wird allen URLs für teilweisen Lizenzerwerb in Inhaltsheadern die Basis-URL am Anfang der partiellen URL hinzugefügt, um eine vollständige URL zu bilden, zu der die Playeranwendung navigieren kann. Der Aufruf von **IWMDRMReader::GetDRMProperty** für **DRM \_ BaseLicenseAcqURL** funktioniert nur in derselben Sitzung wie festgelegt. Die -Eigenschaft wird nicht im Inhaltsheader gespeichert. sie ist dynamisch, und nur die relative URL wird im Inhalt gespeichert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




