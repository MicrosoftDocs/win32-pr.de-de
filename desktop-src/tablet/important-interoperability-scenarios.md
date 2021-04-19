---
description: 'Damit eine Tablet PC-Anwendung effizient mit Ink arbeitet, sollte diese Anwendung folgende Aktionen ausführen können:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Wichtige Interoperabilitäts Szenarien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341184"
---
# <a name="important-interoperability-scenarios"></a>Wichtige Interoperabilitäts Szenarien

Damit eine Tablet PC-Anwendung effizient mit Ink arbeitet, sollte diese Anwendung folgende Aktionen ausführen können:

-   Speichern eines Dokuments im systemeigenen Binärformat der Anwendung, ohne den frei Hand Text des Dokuments zu verlieren.
-   Speichern eines Dokuments in einem beliebigen Format, das von der Anwendung normalerweise unterstützt wird (z. b. html-oder Rich-Text-Format (RTF))
-   Kopieren von frei Hand Eingaben aus einer Anwendung in eine andere mithilfe der Zwischenablage. Dies funktioniert, wenn die andere Anwendung nur ein bestimmtes Format erkennt, z. b. html, RTF oder Bitmap (BMP). Es funktioniert auch, ob die Zielanwendung frei Hand Eingaben erkennt. Wenn frei Hand Eingaben erkannt werden, kann die Zielanwendung die frei Hand Eingaben interpretieren, die als frei Hand Eingaben und nicht nur als Bild kopiert wurden.
-   Kopieren Sie frei Hand Eingaben zusammen mit Text zwischen zwei Anwendungen, die frei Hand Eingaben erkennen, von denen jeder über mehr als ein [**Ink**](inkdisp-class.md) -Objekt verfügt. Hierfür ist HTML, RTF oder ein ähnliches Format erforderlich.
-   Kopieren von frei Hand Eingaben zwischen zwei Anwendungen, von denen jedes über ein [**Ink**](inkdisp-class.md) -Objekt verfügt. Das frei Hand Format (Ink Serialized Format, ISF) ist hierfür ausreichend.
-   Kopieren Sie Freihand aus einer Anwendung, die über mehr als ein [**Ink**](inkdisp-class.md) -Objekt verfügt, in eine Anwendung, die **nur ein frei** Hand Objekt aufweist. In diesem Fall muss die Anwendung mit mehr als einem **Ink** -Objekt in der Lage sein, das frei Hand Format (Ink Serialized Format, ISF) zu liefern.
-   Kopieren von frei Hand Eingaben aus einer Anwendung [**mit einem frei**](inkdisp-class.md) Hand Objekt in eine Anwendung, die über mehr **als ein frei** Hand Objekt verfügt. In diesem Fall muss die Anwendung, die über mehr als ein **Ink** -Objekt verfügt, ISF erkennen können.

 

 



