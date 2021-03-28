---
description: 'Es gibt zwei Arten von Pinseln: logisch und physisch.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informationen zu Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130365"
---
# <a name="about-brushes"></a>Informationen zu Pinseln

Es gibt zwei Arten von Pinseln: logisch und physisch. Ein *logischer Pinsel* ist eine Beschreibung der idealen Bitmap, die eine Anwendung zum Zeichnen von Formen verwendet. Ein *physischer Pinsel* ist die tatsächliche Bitmap, die ein Gerätetreiber basierend auf der logischen Pinsel Definition einer Anwendung erstellt. Weitere Informationen zu Bitmaps finden Sie unter [Bitmaps](bitmaps.md).

Wenn eine Anwendung eine der Funktionen aufruft, die einen Pinsel erstellt, ruft Sie ein Handle ab, das einen logischen Pinsel identifiziert. Wenn die Anwendung dieses Handle an die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion übergibt, erstellt der Gerätetreiber für die entsprechende Anzeige bzw. den entsprechenden Drucker den physischen Pinsel.

In den folgenden Themen werden Pinsel beschrieben:

-   [Pinsel Ursprung](brush-origin.md)
-   [Logische Pinseltypen](logical-brush-types.md)
-   [Muster Block Übertragung](pattern-block-transfer.md)
-   [ICM-aktivierte Pinsel Funktionen](icm-enabled-brush-functions.md)

 

 



