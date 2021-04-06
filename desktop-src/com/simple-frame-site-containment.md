---
title: Kapselung der einfachen Frame Site
description: Kapselung der einfachen Frame Site
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947569"
---
# <a name="simple-frame-site-containment"></a>Kapselung der einfachen Frame Site

Ein Container Steuerelement ist ein ActiveX-Steuerelement, das andere Steuerelemente enthalten kann. Ein Gruppenfeld, das eine Sammlung von Options Feldern enthält, ist ein Beispiel für ein Container Steuerelement. Container Steuerelemente müssen das OLEMISC \_ simpleframe-Statusbit festlegen und sollten die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Implementierung Ihres Containers aufzurufen. **ISimpleFrameSite** muss von einem ActiveX-Steuerelement Container implementiert werden, der Container Steuerelemente unterstützt.

CATID-{157083e0-2368-11CF-87b9-00aa006c8166} CATID \_ simpleframecontrol

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 




