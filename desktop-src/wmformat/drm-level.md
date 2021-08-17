---
title: DRM_Level
description: DIE DRM-Ebene ist ein Lizenzattribut, das vom Windows Media Format SDK beim Erstellen einer lokalen Lizenz für Dateien, die mit DRM Version 1 geschützt \_ werden, definiert wird.
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level windows Media Format
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4767f839c5d21610e7e425aea4a20a52c3cb0d8658848f578a33ca403f4ad60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848683"
---
# <a name="drm_level"></a>\_DRM-Ebene

**DRM \_ Level** ist ein Lizenzattribut, das vom Windows Media Format SDK beim Erstellen einer lokalen Lizenz für Dateien, die mit DRM Version 1 geschützt werden, definiert wird. Sie enthält die Sicherheitsstufe, die die aufrufende Anwendung für den Zugriff auf den Inhalt in der Datei benötigt. Der Standardwert ist 150.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM Level \_

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Die DRM-Sicherheitsstufe einer Anwendung wird durch die spezielle wmstubdrm-Bibliothek bestimmt, mit der sie zur Kompilierzeit verknüpft ist. Weitere Informationen zu diesen Sicherheitsebenen finden Sie unter [Abrufen der erforderlichen DRM-Bibliothek.](obtaining-the-required-drm-library.md) Verwenden [**Sie IWMHeaderInfo::SetAttribute, um diese**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) Eigenschaft beim Schützen von ASF-Dateien mit DRM Version 1 zu festlegen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




