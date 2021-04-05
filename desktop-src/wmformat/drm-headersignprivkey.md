---
title: DRM_HeaderSignPrivKey
description: Die DRM- \_ Eigenschaft "headersignprivkey" enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723488"
---
# <a name="drm_headersignprivkey"></a>DRM \_ headersignprivkey

Die DRM-Eigenschaft " **\_ headersignprivkey** " enthält den privaten Schlüssel, der zum Signieren des ASF-Headers verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm \_ headersignprivkey

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird mit dem [**iwmdrmwriter:: generatesigningkeypair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)generiert. Behalten Sie diesen geheimen Schlüssel bei, und geben Sie den öffentlichen Schlüssel nur mit dem Lizenz Dienst frei. Nachdem Sie diesen Schlüssel festgelegt haben, wird er von der DRM-Komponente zum Signieren des ASF-Datei Headers verwendet (nicht der DRM-Header, der mit den digitalen Signatur Objekt Werten wie z. b. DRM \_ lasignatureprivkey signiert ist). Natürlich ist **DRM \_ headersignprivkey** nicht in der Datei headert enthalten.

Auf diese Eigenschaft kann nicht über das Reader-Objekt zugegriffen werden. Sie kann über das Writer-Objekt mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




