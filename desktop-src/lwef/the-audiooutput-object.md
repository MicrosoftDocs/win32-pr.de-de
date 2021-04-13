---
title: Das Audiooutput-Objekt
description: Das Audiooutput-Objekt
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390313"
---
# <a name="the-audiooutput-object"></a>Das Audiooutput-Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Dieses Objekt ermöglicht den Zugriff auf audioausgabeeigenschaften, die vom Server verwaltet werden. Die Eigenschaften sind schreibgeschützt, aber der Benutzer kann Sie im Eigenschaften Blatt Microsoft-Agent ändern.

Wenn Sie eine Objekt Variable des Typs [**iagentctlaudioobjectex**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**)deklarieren, können Sie nicht auf alle Eigenschaften für das [**Audiooutput**](/windows/desktop/lwef/the-audiooutput-object) -Objekt zugreifen. Obwohl der-Agent auch [**iagentctlaudioobject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**)unterstützt, wird diese letztere Schnittstelle nur aus Gründen der Abwärtskompatibilität bereitgestellt und unterstützt nur diese Eigenschaften in früheren Versionen.

-   [**Aktiviert**](enabled-property-ao.md)
-   [**Sounentffects**](soundeffects-property.md)
-   [**Status**](status-property.md)

 

 