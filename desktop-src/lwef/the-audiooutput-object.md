---
title: Das AudioOutput-Objekt
description: Das AudioOutput-Objekt
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bfef883e5cb40d0a72ec4d848ad0d77f63f58aaeefd907f632e16798be4397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474950"
---
# <a name="the-audiooutput-object"></a>Das AudioOutput-Objekt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Dieses Objekt bietet Zugriff auf Audioausgabeeigenschaften, die vom Server verwaltet werden. Die Eigenschaften sind schreibgeschützt, aber der Benutzer kann sie auf dem Microsoft Agent-Eigenschaftenblatt ändern.

Wenn Sie eine Objektvariable vom Typ [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)deklarieren, können Sie nicht auf alle Eigenschaften für das [**AudioOutput-Objekt**](/windows/desktop/lwef/the-audiooutput-object) zugreifen. Während der -Agent auch [**IAgentCtlAudioObject unterstützt,**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)wird diese zweite Schnittstelle nur aus Gründen der Abwärtskompatibilität bereitgestellt und unterstützt nur diese Eigenschaften in früheren Versionen.

-   [**Aktiviert**](enabled-property-ao.md)
-   [**SoundEffects**](soundeffects-property.md)
-   [**Status**](status-property.md)

 

 