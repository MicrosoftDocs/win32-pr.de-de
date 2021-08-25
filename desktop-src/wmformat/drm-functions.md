---
title: Microsoft Windows Media DRM-Clientfunktionen
description: Microsoft Windows Media DRM-Clientfunktionen
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Medienformat-SDK, Funktionen
- Digital Rights Management (DRM), Funktionen
- DRM (Digital Rights Management), Funktionen
- ERWEITERTE APIs für DEN DRM-Client, Funktionen
- Erweiterte Client-APIs, Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aaf5f3c536027801a85f8d38120e6e14c5d366a6d727498a5bc1d1200cb041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931170"
---
# <a name="microsoft-windows-media-drm-client-functions"></a>Microsoft Windows Media DRM-Clientfunktionen

Die folgenden Funktionen werden als Teil der erweiterten APIs des Microsoft Windows Media DRM-Clients implementiert.



| Funktion                                                             | BESCHREIBUNG                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMDRMCreateProvider**](wmdrmcreateprovider.md)                   | Erstellt eine Klassen factory, die die anderen DRM-Objekte erstellen kann. Diese Funktion erfordert keine Stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Features nicht unterstützen. |
| [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) | Erstellt eine Klassen factory, die die anderen DRM-Objekte erstellen kann. Diese Funktion erfordert eine Stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Funktionen unterstützen.                |
| [**WMDRMShutdown**](wmdrmshutdown.md)                               | Gibt die von den APIs verwendeten Ressourcen frei.                                                                                                                                                            |
| [**WMDRMStartup**](wmdrmstartup.md)                                 | Initialisiert von den APIs verwendete Ressourcen.                                                                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](drm-programming-reference.md)
</dt> </dl>

 

 




