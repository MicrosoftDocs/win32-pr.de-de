---
title: Erstellen geschützter Dateien
description: Erstellen geschützter Dateien
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media-Format-SDK, erstellen geschützter Dateien
- Windows Media-Format-SDK, geschützte Dateien
- Advanced Systems Format (ASF), erstellen geschützter Dateien
- ASF (Advanced Systems Format), erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF), wmstubdrm. lib
- ASF (Advanced Systems Format), wmstubdrm. lib
- Wmstubdrm. lib, erstellen geschützter Dateien
- Wmstubdrm. lib, geschützte Dateien
- Digital Rights Management (DRM), wmstubdrm. lib
- DRM (Digital Rights Management), wmstubdrm. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314261"
---
# <a name="creating-protected-files"></a>Erstellen geschützter Dateien

Um geschützte digitale Mediendateien mithilfe von DRM Version 1 oder DRM Version 7 und höher zu erstellen, verknüpfen Sie eine Verknüpfung mit der Datei "wmstubdrm. lib", die Sie von Microsoft erhalten haben, und erstellen Sie das Writer-Objekt. Verwenden Sie für den Schutz von Version 1 die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle zum Festlegen der DRM-Attribute, die Sie anwenden möchten. Verwenden Sie für die Versionen 7 und höher die [**iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) -Schnittstellen Methoden.

In den folgenden Themen wird ausführlich beschrieben, wie Sie Dateien schützen.

-   [Schützen von Dateien mit DRM-Version 1](protecting-files-with-drm-version-1.md)
-   [Schützen von Dateien mit DRM-Version 7 oder höher](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attribut Liste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**DRM-Versionen**](drm-versions.md)
</dt> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Abrufen der erforderlichen DRM-Bibliothek**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Geschützte Dateien werden gelesen.**](reading-protected-files.md)
</dt> </dl>

 

 




