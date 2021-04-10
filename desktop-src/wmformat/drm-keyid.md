---
title: DRM_KeyID
description: Das DRM- \_ keyid-Attribut enthält den Schlüssel Bezeichner.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038588"
---
# <a name="drm_keyid"></a>DRM- \_ Schlüssel-ID

Das **DRM- \_ keyid** -Attribut enthält den Schlüssel Bezeichner.

## <a name="global-constant"></a>Globale Konstante

Schlüssel-ID für g \_ wszwmdrm \_

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur für den DRM-Inhalt der DRM-Version 7 vorhanden. Sie kann mithilfe von [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) festgelegt werden und kann mit " [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)" abgerufen werden. Das gleiche Datei Attribut kann mit der [**DRM- \_ drmHeader- \_ keyid**](drm-drmheader-keyid.md)abgerufen werden.

Die Schlüssel-ID wird zusammen mit dem Schlüssel-Seed zum Erstellen des Inhalts Schlüssels verwendet, der zum Verschlüsseln und Entschlüsseln der Datei verwendet wird. Die Writer-Anwendung verwendet die Schlüssel-ID, um die Datei zu verschlüsseln, und speichert dann die Schlüssel-ID im Dateiheader. Wenn eine Player Anwendung eine Lizenz für eine Datei anfordert, sendet die DRM-Komponente die Schlüssel-ID (zusammen mit dem Rest des DRM-Headers) an den Lizenzserver. Der Lizenzserver, der über den Wert des geheimen Schlüssels verfügt, verwendet ihn und die Schlüssel-ID, um einen Schlüssel für die Datei zu erstellen, der dann zusammen mit den verschiedenen rechten, die auf die Datei angewendet werden, in eine Lizenz eingefügt wird.

In der Regel wird ein Schlüssel-Seed mit vielen Schlüssel-IDs verwendet. Der Schlüsselwert ist ein geheimer Schlüssel, der nur vom Inhalts Ersteller und dem Lizenz Verteiler gemeinsam verwendet wird. Die Schlüssel-ID wird von DRM-Client Anwendungen verwendet und im DRM-Header unverschlüsselt gespeichert.

Dieses Attribut ist mit der [**DRM- \_ drmHeader- \_ keyid**](drm-drmheader-keyid.md)identisch.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




