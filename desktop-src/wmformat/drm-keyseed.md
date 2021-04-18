---
title: DRM_KeySeed
description: Die DRM- \_ keyseed-Eigenschaft enthält den schlüsselseed, der in Verbindung mit der keyid verwendet wird, um den Schlüssel zu erstellen.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106340685"
---
# <a name="drm_keyseed"></a>DRM- \_ keyseed

Die **DRM- \_ keyseed** -Eigenschaft enthält den schlüsselseed, der in Verbindung mit der keyid verwendet wird, um den Schlüssel zu erstellen.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ keyseed

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)festgelegt werden. Das Reader-Objekt ist nicht verfügbar.

Ein schlüsselseed wird normalerweise verwendet, um mehrere Dateien oder Dateigruppen zu schützen, z. b. alle Dateien, die von einem Lizenzserver ausgestellt werden, oder möglicherweise alle Dateien eines bestimmten Künstlers. Die keyid ist jedoch für jede Datei eindeutig.

Der Schlüssel-Seed muss ein Geheimnis bleiben, das nur zwischen dem Inhalts Ersteller und dem Lizenz Verteiler freigegeben ist. Dieser Wert wird nicht im DRM-Header gespeichert und ist weder für DRM-Player-Anwendungen noch für den Zugriff verfügbar.

Ein neuer Schlüssel Ausgangswert kann mithilfe der [**iwmdrmwriter:: generatekeyseed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) -Methode oder durch andere geeignete Mittel generiert werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




