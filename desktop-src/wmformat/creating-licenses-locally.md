---
title: Lokales Erstellen von Lizenzen
description: Lokales Erstellen von Lizenzen
ms.assetid: 151dd231-26a9-4203-84e1-446a07c1e07a
keywords:
- Windows Medienformat-SDK, lokales Erstellen von Lizenzen
- Windows Medienformat-SDK, Lizenzen
- Digital Rights Management (DRM), lokales Erstellen von Lizenzen
- DRM (Digital Rights Management), lokales Erstellen von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte DRM-Client-APIs, lokales Erstellen von Lizenzen
- Erweiterte Client-APIs, lokales Erstellen von Lizenzen
- Lizenzen,lokales Erstellen von Lizenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1a889e83f093cbd60043b299b7174a6c963663962a66454c5707060e76232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433906"
---
# <a name="creating-licenses-locally"></a>Lokales Erstellen von Lizenzen

Unter bestimmten Umständen, z. B. während [des DRM-Imports,](drm-import.md)können Sie Eigene Lizenzen erstellen. Windows Medien-DRM-Lizenzen können auf verschiedene Weise geschrieben werden, aber um Ihre eigene Lizenz zu erstellen, müssen Sie das binäre Schema Extensible Media Rights (XMR) verwenden. Weitere Informationen finden Sie unter [Erstellen einer XMR-Lizenz.](building-an-xmr-license.md)

Wenn Sie eine Lizenz erstellen, können Sie sie dem lokalen Lizenzspeicher hinzufügen, indem Sie die [**IWMDRMLicenseManagement::StoreLicense-Methode**](iwmdrmlicensemanagement-storelicense.md) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Erstellen einer XMR-Lizenz**](building-an-xmr-license.md)
</dt> </dl>

 

 




