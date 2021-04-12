---
title: DRM_LASignaturePrivKey
description: Die DRM- \_ lasignatureprivkey-Eigenschaft enthält den privaten Schlüssel, der zum Verschlüsseln des DRM-Headers verwendet wird.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389916"
---
# <a name="drm_lasignatureprivkey"></a>DRM- \_ lasignatureprivkey

Die **DRM- \_ lasignatureprivkey** -Eigenschaft enthält den privaten Schlüssel, der zum Verschlüsseln des DRM-Headers verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ lasignatureprivkey

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann mit der [**iwmdrmwriter:: generatesigningkeypair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) -Methode generiert werden. Diese Eigenschaft sollte ein Geheimnis bleiben, das nur vom Inhalts Ersteller bekannt ist. Diese Eigenschaft kann mit der [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) -Methode festgelegt werden. Das Reader-Objekt ist nicht verfügbar.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




