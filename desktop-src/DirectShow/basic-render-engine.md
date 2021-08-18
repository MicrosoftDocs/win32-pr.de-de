---
description: Grundlegende Render-Engine
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Grundlegende Render-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955572"
---
# <a name="basic-render-engine"></a>Grundlegende Render-Engine

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das Basic Render Engine-Objekt rendert eine nicht komprimierte Ausgabe von einer Zeitachse. Um dieses Objekt zu erstellen, rufen Sie **CoCreateInstance** auf. Verwenden Sie für komprimierte Ausgaben die intelligente Render-Engine. Der Klassenbezeichner ist CLSID \_ RenderEngine.

Die Basic-Render-Engine macht die folgenden Schnittstellen verfügbar:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   Iobjectwithsite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern eines Project](rendering-a-project.md)
</dt> <dt>

[Intelligente Render-Engine](smart-render-engine.md)
</dt> </dl>

 

 



