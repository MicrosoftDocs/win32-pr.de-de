---
description: 'Es gibt zwei Arten von Pinseln: logisch und physisch.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informationen zu Pinseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c94ea9dac021a013ccc4ef624f9b00a3234102ac905999cb7c085148be91b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602790"
---
# <a name="about-brushes"></a>Informationen zu Pinseln

Es gibt zwei Arten von Pinseln: logisch und physisch. Ein *logischer Pinsel* ist eine Beschreibung der idealen Bitmap, die eine Anwendung zum Zeichnen von Formen verwendet. Ein *physischer Pinsel* ist die tatsächliche Bitmap, die ein Gerätetreiber basierend auf der Definition eines logischen Pinsels einer Anwendung erstellt. Weitere Informationen zu Bitmaps finden Sie unter [Bitmaps.](bitmaps.md)

Wenn eine Anwendung eine der Funktionen aufruft, die einen Pinsel erstellt, ruft sie ein Handle ab, das einen logischen Pinsel identifiziert. Wenn die Anwendung dieses Handle an die [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) übergibt, erstellt der Gerätetreiber für die entsprechende Anzeige oder den entsprechenden Drucker den physischen Pinsel.

In den folgenden Themen werden Pinsel beschrieben:

-   [Pinselursprung](brush-origin.md)
-   [Logische Pinseltypen](logical-brush-types.md)
-   [Musterblockübertragung](pattern-block-transfer.md)
-   [ICM-fähige Pinselfunktionen](icm-enabled-brush-functions.md)

 

 



