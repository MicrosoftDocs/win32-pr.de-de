---
title: Erstellen geschützter Dateien
description: Erstellen geschützter Dateien
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Medienformat-SDK, Erstellen geschützter Dateien
- Windows Medienformat-SDK, geschützte Dateien
- Advanced Systems Format (ASF), Erstellen geschützter Dateien
- ASF (Advanced Systems Format), Erstellen geschützter Dateien
- Advanced Systems Format (ASF), geschützte Dateien
- ASF (Advanced Systems Format), geschützte Dateien
- Advanced Systems Format (ASF),WMStubDRM.lib
- ASF (Advanced Systems Format), WMStubDRM.lib
- WMStubDRM.lib, Erstellen geschützter Dateien
- WMStubDRM.lib,geschützte Dateien
- Digital Rights Management (DRM), WMStubDRM.lib
- DRM (Digital Rights Management), WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809470"
---
# <a name="creating-protected-files"></a>Erstellen geschützter Dateien

Um geschützte digitale Mediendateien mit DRM Version 1 oder DRM Version 7 und höher zu erstellen, verknüpfen Sie die Datei WMStubDRM.lib, die Sie von Microsoft erhalten haben, und erstellen Sie das Writer-Objekt. Verwenden Sie für den Schutz der Version 1 die [**IWMHeaderInfo-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) um die DRM-Attribute zu festlegen, die Sie anwenden möchten. Verwenden Sie für Version 7 und höher die [**METHODEN der IWMDRMWriter-Schnittstelle.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)

In den folgenden Themen wird ausführlich beschrieben, wie Dateien geschützt werden.

-   [Schützen von Dateien mit DRM Version 1](protecting-files-with-drm-version-1.md)
-   [Schützen von Dateien mit DRM Version 7 oder höher](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DRM-Attributliste**](drm-attribute-list.md)
</dt> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> <dt>

[**DRM-Versionen**](drm-versions.md)
</dt> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**Abrufen der erforderlichen DRM-Bibliothek**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Lesen geschützter Dateien**](reading-protected-files.md)
</dt> </dl>

 

 




