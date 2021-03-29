---
description: Windows unterstützt fünf Grafikmodi, die es einer Anwendung ermöglichen, anzugeben, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw. Diese Modi, die auf einem DC gespeichert werden, werden in der folgenden Tabelle beschrieben.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Grafikmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528343"
---
# <a name="graphic-modes"></a>Grafikmodi

Windows unterstützt fünf Grafikmodi, die es einer Anwendung ermöglichen, anzugeben, wie Farben gemischt werden, wo die Ausgabe angezeigt wird, wie die Ausgabe skaliert wird usw. Diese Modi, die auf einem DC gespeichert werden, werden in der folgenden Tabelle beschrieben.



| Grafikmodus | BESCHREIBUNG                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| Hintergrund    | Definiert, wie Hintergrundfarben mit vorhandenen Fenstern oder Bildschirmfarben für Bitmap-und Text Vorgänge gemischt werden.              |
| Zeichnung       | Definiert, wie Vorder Grundfarben mit vorhandenen Fenstern oder Bildschirmfarben für Stift-, Pinsel-, Bitmap-und Text Vorgänge gemischt werden. |
| Zuordnung       | Definiert, wie die Grafikausgabe aus dem logischen (oder weltweiten) Raum auf dem Fenster, dem Bildschirm oder dem Drucker Papier zugeordnet wird.             |
| Polygon-Füllung  | Definiert, wie das Pinsel Muster verwendet wird, um das innere komplexer Regionen auszufüllen.                                             |
| Dehnung    | Definiert, wie Bitmapfarben mit vorhandenen Fenstern oder Bildschirmfarben gemischt werden, wenn die Bitmap komprimiert (oder zentral herunterskaliert) wird.  |



 

Wie bei grafischen Objekten initialisiert das System einen DC mit Standard Grafikmodi. Eine Anwendung kann diese Standard Modi abrufen und überprüfen, indem Sie die folgenden Funktionen aufrufen.



| Grafikmodus | Funktion                                       |
|---------------|------------------------------------------------|
| Hintergrund    | [**Getbkmode**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| Zeichnung       | [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| Zuordnung       | [**Getmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| Polygon-Füllung  | [**Getpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| Dehnung    | [**Getstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

Eine Anwendung kann die Standard Modi ändern, indem Sie eine der folgenden Funktionen aufrufen.



| Grafikmodus | Funktion                                       |
|---------------|------------------------------------------------|
| Hintergrund    | [**Setbkmode**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| Zeichnung       | [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| Zuordnung       | [**Setmapmode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| Polygon-Füllung  | [**Setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| Dehnung    | [**Setstretchbltmode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



