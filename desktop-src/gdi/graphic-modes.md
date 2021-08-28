---
description: Windows unterstützt fünf Grafikmodi, mit denen eine Anwendung angeben kann, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw. Diese Modi, die in einem Domänencontroller gespeichert sind, werden in der folgenden Tabelle beschrieben.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Grafikmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c36461935c8279e38e09afe9f7802e2f758d1cf45380beaa16d1911f4ed965f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558770"
---
# <a name="graphic-modes"></a>Grafikmodi

Windows unterstützt fünf Grafikmodi, mit denen eine Anwendung angeben kann, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw. Diese Modi, die in einem Domänencontroller gespeichert sind, werden in der folgenden Tabelle beschrieben.



| Grafikmodus | Beschreibung                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Hintergrund    | Definiert, wie Hintergrundfarben mit vorhandenen Fenster- oder Bildschirmfarben für Bitmap- und Textvorgänge kombiniert werden.              |
| Zeichnung       | Definiert, wie Vordergrundfarben mit vorhandenen Fenster- oder Bildschirmfarben für Stift-, Pinsel-, Bitmap- und Textoperationen kombiniert werden. |
| Zuordnung       | Definiert, wie die Grafikausgabe aus dem logischen (oder weltweiten) Raum auf dem Fenster, Bildschirm oder Druckerdokument zugeordnet wird.             |
| Polygonfüllung  | Definiert, wie das Pinselmuster verwendet wird, um das Innere komplexer Bereiche zu füllen.                                             |
| Stretching    | Definiert, wie Bitmapfarben mit vorhandenen Fenster- oder Bildschirmfarben kombiniert werden, wenn die Bitmap komprimiert (oder herunterskaliert) wird.  |



 

Wie bei grafikgrafischen Objekten initialisiert das System einen DC mit Standardgrafikmodi. Eine Anwendung kann diese Standardmodi abrufen und untersuchen, indem sie die folgenden Funktionen aufruft.



| Grafikmodus | Funktion                                       |
|---------------|------------------------------------------------|
| Hintergrund    | [**GetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Zeichnung       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Zuordnung       | [**GetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Polygonfüllung  | [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Stretching    | [**GetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Eine Anwendung kann die Standardmodi ändern, indem sie eine der folgenden Funktionen aufruft.



| Grafikmodus | Funktion                                       |
|---------------|------------------------------------------------|
| Hintergrund    | [**SetBkMode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Zeichnung       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Zuordnung       | [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Polygonfüllung  | [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Stretching    | [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



