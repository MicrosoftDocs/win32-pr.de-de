---
title: Fenster Rückruf Dienste
description: Fenster Rückruf Dienste
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- Multimedia-Audiodaten, Fenster Rückruf Dienste
- Audiodienste, Fenster Rückruf Dienste
- Audiomixer, Fenster Rückruf Dienste
- Mixer, Fenster Rückruf Dienste
- Fenster Rückruf Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472972"
---
# <a name="window-callback-services"></a>Fenster Rückruf Dienste

Die Mixer Dienste stellen Fenster Rückruf Dienste bereit, sodass Ihre Anwendung Nachrichten von Mixer-Treibern verarbeiten kann. Wenn Sie diese Dienste verwenden möchten, geben Sie das Rückruf \_ Fenster-Flag im *fdwopen* -Parameter und ein Fenster Handle im *dwcallback* -Parameter der [**mixeropen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) -Funktion an. Treiber Meldungen werden an die Fenster Prozedur Funktion für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird. Die Nachrichten sind spezifisch für den audiogerätetyp.

 

 