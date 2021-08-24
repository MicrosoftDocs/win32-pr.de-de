---
title: DRM_KeySeed
description: Die DRM \_ KeySeed-Eigenschaft enthält den Schlüsselseeding, der in Verbindung mit der KeyID zum Erstellen des Schlüssels verwendet wird.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46766dc5754bde33c00af250f03a54caf3c12c607ec14da858ac638a70f79baf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658970"
---
# <a name="drm_keyseed"></a>DRM \_ KeySeed

Die **DRM \_ KeySeed-Eigenschaft** enthält den Schlüsselseeding, der in Verbindung mit der KeyID zum Erstellen des Schlüssels verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM \_ KeySeed

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYPZEICHENFOLGE**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann mit [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden. Das Readerobjekt kann nicht darauf zugreifen.

Ein Schlüsselwert wird in der Regel verwendet, um mehrere Dateien oder Gruppen von Dateien zu schützen, z. B. alle Dateien, die von einem Lizenzserver ausgestellt wurden, oder möglicherweise alle Dateien eines bestimmten Interpreten. Die KeyID ist jedoch für jede Datei eindeutig.

Der Ausgangswert des Schlüssels muss ein Geheimnis bleiben, das nur vom Inhaltsersteller und dem Lizenzverteiler gemeinsam genutzt wird. Dieser Wert wird nicht im DRM-Header gespeichert und ist weder für DRM-Playeranwendungen erforderlich noch zugänglich.

Ein neuer Schlüsselseeding kann mithilfe der [**IWMDRMWriter::GenerateKeySeed-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) oder auf andere geeignete Weise generiert werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




