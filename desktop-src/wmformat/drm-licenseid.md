---
title: DRM_LicenseID
description: Die \_ DRM-LicenseID-Eigenschaft enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der derzeit geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- DRM_LicenseID Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9dea32903de18dd1bde8f132b8acf993d3eba2deb0d45c814f0572ce8591ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930950"
---
# <a name="drm_licenseid"></a>\_DRM-Lizenz-ID

Die **\_ DRM-LicenseID-Eigenschaft** enthält eine Zeichenfolge, die aus der Lizenz abgerufen wird, die der derzeit geöffneten Datei zugeordnet ist, die diese Lizenz eindeutig identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist nur mit DRM Version 7-Inhalt vorhanden. Sie kann mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt und mit [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen werden.

Die Lizenz-ID wird in einer Lizenz und nicht in einer ASF-Datei gespeichert. Jede einzelne Lizenz verfügt über eine eindeutige ID, die vom Lizenzgenerator zum Zeitpunkt der Erstellung der Lizenz zugewiesen wird. Wenn Sie z. B. zwei Lizenzen für denselben Inhalt erhalten, verfügt jede über ein anderes LicenseID-Attribut. In der Regel müssen Anwendungen diesen Wert nicht abrufen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




