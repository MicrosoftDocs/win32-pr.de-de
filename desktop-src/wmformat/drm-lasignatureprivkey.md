---
title: DRM_LASignaturePrivKey
description: Die DRM-Eigenschaft LASignaturePrivKey enthält den privaten Schlüssel, der zum \_ Verschlüsseln des DRM-Headers verwendet wird.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704324"
---
# <a name="drm_lasignatureprivkey"></a>DRM \_ LASignaturePrivKey

Die **\_ DRM-Eigenschaft LASignaturePrivKey enthält** den privaten Schlüssel, der zum Verschlüsseln des DRM-Headers verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Datentyp

**\_WMT-TYPZEICHENFOLGE \_**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann mit der [**IWMDRMWriter::GenerateSigningKeyPair-Methode generiert**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) werden. Diese Eigenschaft sollte ein Geheimnis bleiben, das nur dem Inhaltsersteller bekannt ist. Diese Eigenschaft kann mit der [**IWMDRMWriter::SetDRMAttribute-Methode festgelegt**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) werden. Es ist für das Readerobjekt nicht zugänglich.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




