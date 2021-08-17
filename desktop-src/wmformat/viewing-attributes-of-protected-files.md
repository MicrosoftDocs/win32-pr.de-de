---
title: Anzeigen von Attributen von geschützten Dateien
description: Anzeigen von Attributen von geschützten Dateien
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Medienformat-SDK, Anzeigen von Attributen geschützter Dateien
- Windows Medienformat-SDK, Attribute geschützter Dateien
- Windows Medienformat-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Anzeigen von Attributen geschützter Dateien
- ASF (Advanced Systems Format), Anzeigen von Attributen geschützter Dateien
- Advanced Systems Format (ASF), Attribute geschützter Dateien
- ASF (Advanced Systems Format), Attribute von geschützten Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Digital Rights Management (DRM), Anzeigen von Attributen geschützter Dateien
- DRM (Verwaltung digitaler Rechte),Anzeigen von Attributen geschützter Dateien
- Digital Rights Management (DRM), Attribute geschützter Dateien
- DRM (Verwaltung digitaler Rechte),Attribute geschützter Dateien
- Digital Rights Management (DRM), geschützte Dateien
- DRM (Digital Rights Management), geschützte Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cd09e61dbd5515d643cbffe8cce809d0f828e8d153858c78ee52db7e714344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844913"
---
# <a name="viewing-attributes-of-protected-files"></a>Anzeigen von Attributen von geschützten Dateien

In einigen Szenarien müssen Sie möglicherweise bestimmte DRM-Attribute in einer Datei abrufen, ohne tatsächlich auf den Inhalt der Datei zuzugreifen. Diese Funktion ist z. B. in Anwendungen nützlich, die Batches von Dateien auf unterschiedliche Weise basierend auf Informationen im Dateiheader verarbeiten. In früheren Versionen des Windows Media Format SDK mussten Anwendungen eine Verknüpfung mit der statischen DRM-Bibliothek erstellen, um geschützte Dateien zu öffnen. Anwendungen, die nicht über die DRM-Bibliothek verfügen, können die [**IWMDRMEditor::GetDRMProperty-Schnittstelle**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) für das Metadaten-Editor-Objekt verwenden, um bestimmte DRM-Attribute zu untersuchen.

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMEditor-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




