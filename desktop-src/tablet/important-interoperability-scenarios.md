---
description: Damit eine Tablet PC-Anwendung effektiv mit Ink betrieben werden kann, sollte diese Anwendung in der Lage sein,
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Wichtige Interoperabilitätsszenarien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42f021cd1a8dbb3a8b65780b71db66a4c43fa18097f967f794c1a2b2c3ce16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718959"
---
# <a name="important-interoperability-scenarios"></a>Wichtige Interoperabilitätsszenarien

Damit eine Tablet PC-Anwendung effektiv mit Ink betrieben werden kann, sollte diese Anwendung in der Lage sein,

-   Speichern Sie ein Dokument im nativen Binärformat der Anwendung, ohne die Ink-Datei des Dokuments zu verlieren.
-   Speichern Sie ein Dokument in einem beliebigen Format, das die Anwendung normalerweise unterstützt (z. B. HTML oder Rich Text Format (RTF)), ohne die Ink-Datei des Dokuments zu verlieren.
-   Kopieren Sie Ink aus einer Anwendung in eine andere, indem Sie die Zwischenablage verwenden. Dies funktioniert, wenn die andere Anwendung nur ein bestimmtes Format erkennt, z. B. HTML, RTF oder Bitmap (BMP). Es funktioniert auch, ob die Zielanwendung Ink erkennt. Wenn sie Ink erkennt, kann die Zielanwendung die Ink-Datei interpretieren, die als Ink und nicht nur als Bild kopiert wurde.
-   Kopieren Sie Ink zusammen mit Text zwischen zwei Anwendungen, die Ink erkennen, von denen jede über mehr als ein [**Ink-Objekt**](inkdisp-class.md) verfügt. Dies erfordert HTML, RTF oder ein ähnliches Format.
-   Kopieren Sie Ink zwischen zwei Anwendungen, von denen jede über ein [**Ink-Objekt**](inkdisp-class.md) verfügt. serialisiertes Freihandformat (ISF) ist dafür ausreichend.
-   Kopieren Sie Ink aus einer Anwendung, die über mehr als ein [**Ink-Objekt**](inkdisp-class.md) verfügt, in eine Anwendung, die nur über ein **Ink-Objekt** verfügt. In diesem Fall muss die Anwendung, die über mehr als ein **Ink-Objekt** verfügt, in der Lage sein, serialisiertes Freihandformat (ISF) zu erzeugen.
-   Kopieren Sie Ink aus einer Anwendung, die über ein [**Ink-Objekt**](inkdisp-class.md) verfügt, in eine Anwendung mit mehr als einem **Ink-Objekt.** In diesem Fall muss die Anwendung, die über mehr als ein **Ink-Objekt** verfügt, ISF erkennen können.

 

 



