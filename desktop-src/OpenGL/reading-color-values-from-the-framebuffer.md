---
title: Lesen von Farbwerten aus dem Framebuffer
description: Wenn Sie Funktionen verwenden, die Farbwerte aus dem Framepuffer zurücklesen, beachten Sie die Unterschiede zwischen dem Lesen von RGBA-Werten und Farbindexwerten auf Geräten mit richtiger Farbe und auf palettenbasierten Geräten.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL unter Windows, Lesen von Farbwerten aus Framepuffern
- Lesen von Farbwerten aus framebuffers OpenGL
- framebuffers,reading color values OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65beb6dae04019637fc8683220ce12e671c4a52d4f015ae9f8d45e70db67bb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794767"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lesen von Farbwerten aus dem Framebuffer

Wenn Sie Funktionen verwenden, die Farbwerte aus dem Framepuffer zurücklesen, beachten Sie die Unterschiede zwischen dem Lesen von RGBA-Werten und Farbindexwerten auf Geräten mit richtiger Farbe und auf palettenbasierten Geräten.

Auf einem Gerät mit richtiger Farbe:

-   RGBA-Werte sind auf den Kanal im Gerät beschränkt.
-   Farbindexwerte werden als RGBA-Werte im Framepuffer gespeichert. Wenn Sie diese Werte verwenden, müssen Sie eine umgekehrte Übersetzung von RGBA in den logischen Palettenindex ausführen. Wenn zwei logische Indizes dieselben RGBA-Werte haben, kann der falsche Index zurückgegeben werden.

Auf einem palettenbasierten Gerät:

-   RGBA-Werte werden aus einem Index in der Systempalette gelesen. Der logische Index wird aus einer umgekehrten Tabelle ermittelt, und die RGBA-Komponenten werden extrahiert.
-   Farbindexwerte werden aus einem Index in die Systempalette gelesen, und eine umgekehrte Tabelle wird verwendet, um den logischen Palettenindex zu erhalten.

 

 




