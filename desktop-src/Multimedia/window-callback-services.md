---
title: Rückrufdienste für Fenster
description: Rückrufdienste für Fenster
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- Multimediaaudio, Fensterrückrufdienste
- Audio, Fensterrückrufdienste
- Audiomixer, Fensterrückrufdienste
- Mixer, Fensterrückrufdienste
- Fensterrückrufdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0248928d339dc6c1737ee9dc47f72bac0fb42fe76774e6062177c29064b44257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781410"
---
# <a name="window-callback-services"></a>Rückrufdienste für Fenster

Die Mixerdienste stellen Fensterrückrufdienste bereit, sodass Ihre Anwendung Nachrichten von Mixertreibern verarbeiten kann. Um diese Dienste zu verwenden, geben Sie das \_ CALLBACK WINDOW-Flag im *fdwOpen-Parameter* und ein Fensterhandle im *dwCallback-Parameter* der [**mixerOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) an. Treibermeldungen werden an die Fensterprozedurfunktion für das Fenster gesendet, das durch das Handle in *dwCallback* identifiziert wird. Die Nachrichten sind spezifisch für den Audiogerätetyp.

 

 