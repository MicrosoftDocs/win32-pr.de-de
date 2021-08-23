---
title: DRM_HeaderSignPrivKey
description: Die \_ DRM-Eigenschaft HeaderSignPrivKey enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7f8cc90e509294d9de9d3577ad5a2d56b61eb3a471f9b493e555c0f1ecf824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547610"
---
# <a name="drm_headersignprivkey"></a>\_DRM-HeaderSignPrivKey

Die **\_ DRM-Eigenschaft HeaderSignPrivKey** enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird mit [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)generiert. Behalten Sie diesen Geheimschlüssel bei, und geben Sie den öffentlichen Schlüssel nur für den Lizenzdienst frei. Nachdem Sie diesen Schlüssel festgelegt haben, verwendet die DRM-Komponente ihn zum Signieren des ASF-Dateiheaders (nicht des DRM-Headers, der mit den Digitalen Signaturobjektwerten wie DRM \_ LASignaturePrivKey signiert ist). Natürlich ist **DRM \_ HeaderSignPrivKey** nicht im Dateiheader enthalten.

Auf diese Eigenschaft kann nicht über das Readerobjekt zugegriffen werden. Sie kann über das Writer-Objekt mithilfe von [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




