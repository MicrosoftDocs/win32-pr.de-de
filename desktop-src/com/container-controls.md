---
title: Containersteuerelemente
description: Containersteuerelemente
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896440"
---
# <a name="container-controls"></a>Containersteuerelemente

Wie oben beschrieben, sind Containersteuerelemente ActiveX, die andere Steuerelemente visuell enthalten. Die ActiveX-Steuerelementarchitektur gibt die [**ISimpleFrameSite-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) an, um Containersteuerelemente zu aktivieren. Container können auch Containersteuerelemente unterstützen, ohne **ISimpleFrameSite zu** unterstützen, obwohl das Verhalten nicht garantiert werden kann. Aus diesem Grund gibt es eine Komponentenkategorie für SimpleFrameSite-Steuerelemente, bei denen die vollständige Funktionalität dieser Schnittstelle erforderlich ist.

Um Containersteuerelemente ohne Implementierung von [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)zu unterstützen, muss ein ActiveX-Steuerelementcontainer:

-   Aktivieren Sie alle Steuerelemente jederzeit.
-   Überleiten Sie die enthaltenen Steuerelemente an den hWnd des enthaltenden Steuerelements.
-   Bleiben Sie das übergeordnete Element des Containersteuer elements.

 

 




