---
title: Anzeigen der Attribute geschützter Dateien
description: Anzeigen der Attribute geschützter Dateien
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media-Format-SDK, Anzeigen von Attributen geschützter Dateien
- Windows Media-Format-SDK, Attribute geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Anzeigen von Attributen geschützter Dateien
- ASF (Advanced Systems Format), Anzeigen von Attributen geschützter Dateien
- Advanced Systems Format (ASF), Attribute geschützter Dateien
- ASF (Advanced Systems Format), Attribute geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Digital Rights Management (DRM), Anzeigen der Attribute geschützter Dateien
- DRM (Digital Rights Management), Anzeigen der Attribute geschützter Dateien
- Digital Rights Management (DRM), Attribute geschützter Dateien
- DRM (Digital Rights Management), Attribute geschützter Dateien
- Digital Rights Management (DRM), geschützte Dateien
- DRM (Digital Rights Management), geschützte Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723397"
---
# <a name="viewing-attributes-of-protected-files"></a>Anzeigen der Attribute geschützter Dateien

In einigen Szenarien müssen Sie möglicherweise bestimmte DRM-Attribute in einer Datei abrufen, ohne tatsächlich auf den Inhalt der Datei zuzugreifen. Diese Funktion ist beispielsweise bei Anwendungen nützlich, die Datei Batches auf verschiedene Weise auf der Grundlage von Informationen im Dateiheader verarbeiten. In früheren Versionen des SDK für den Windows Media-Format mussten Anwendungen eine Verknüpfung mit der statischen DRM-Bibliothek herstellen, um geschützte Dateien zu öffnen. Anwendungen, die keine DRM-Bibliothek haben, können die [**iwmdrmeditor:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) -Schnittstelle für das Metadaten-Editor-Objekt verwenden, um bestimmte DRM-Attribute zu untersuchen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Iwmdrmeditor-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




