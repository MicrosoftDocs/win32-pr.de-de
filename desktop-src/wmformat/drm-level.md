---
title: DRM_Level
description: DRM- \_ Ebene ist ein Lizenz Attribut, das das Windows Media-Format SDK festlegt, wenn es eine lokale Lizenz für Dateien erstellt, die mit DRM-Version 1 geschützt sind.
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314350"
---
# <a name="drm_level"></a>DRM- \_ Ebene

**DRM \_ Level** ist ein Lizenz Attribut, das vom Windows Media-Format SDK festgelegt wird, wenn es eine lokale Lizenz für Dateien erstellt, die mit DRM-Version 1 geschützt sind. Sie enthält die Sicherheitsstufe, die von der aufrufenden Anwendung benötigt werden muss, um auf den Inhalt in der Datei zuzugreifen. Der Standardwert ist 150.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Ebene

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Die DRM-Sicherheitsstufe einer Anwendung wird von der jeweiligen wmstubdrm-Bibliothek bestimmt, mit der zum Zeitpunkt der Kompilierung eine Verknüpfung besteht. Weitere Informationen zu diesen Sicherheitsstufen finden Sie unter Abrufen [der erforderlichen DRM-Bibliothek](obtaining-the-required-drm-library.md). Verwenden Sie [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , um diese Eigenschaft beim Schutz von ASF-Dateien mit DRM-Version 1 festzulegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




